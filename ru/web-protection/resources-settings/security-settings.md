---
id: 269
seoTitle: Дополнительные настройки безопасности, настройка фаервола — Solar Space
seoDescription: Дополнительные настройки безопасности — настройка фаервола. Примеры настроек для популярных фаерволов — iptables, UFW, nftables, firewalld
displayName: Дополнительные настройки безопасности
order: 5
published: true
historyName: Дополнительные настройки безопасности
historyDescription: Информация по дополнительным настройкам безопасности Solar Space
---

# [Дополнительные настройки безопасности](additional-security-settings)

## [Настройка фаервола](configuring-firewall)

Мы рекомендуем запретить подключения к целевому серверу с любых адресов, кроме адресов Solar Space, с которых осуществляется проксирование запросов. Для этого в фаерволе создайте правила на блокировку любых запросов, кроме запросов из доверенных сетей Solar Space.

Список сетей, которые необходимо добавить в белый список фаервола:

* **93.185.164.0/25**

## [Примеры настроек для популярных фаерволов](examples-of-settings-for-popular-firewalls)

> **INFO**
>
> #### Обратите внимание
>
> Данные настройки приведены исключительно в качестве примеров. Перед их применением убедитесь, что они соответствуют требованиям вашего проекта и не приведут к сбоям в его работе

### [Пример настроек iptables](example-of-iptables-settings)

```
sudo iptables -A INPUT -s 93.185.164.0/25 -p tcp --dport 80 -j ACCEPT
sudo iptables -A INPUT -s 93.185.164.0/25 -p tcp --dport 443 -j ACCEPT
sudo iptables -A INPUT -p tcp --dport 80 -j DROP
sudo iptables -A INPUT -p tcp --dport 443 -j DROP
```

### [Пример настроек UFW](example-of-ufm-settings)

```
sudo ufw allow from 93.185.164.0/25 to any port 80 proto tcp comment "Allow HTTP SS"
sudo ufw allow from 93.185.164.0/25 to any port 443 proto tcp comment "Allow HTTPS SS"
sudo ufw deny to any port 80 proto tcp comment "Deny all other HTTP traffic"
sudo ufw deny to any port 443 proto tcp comment "Deny all other HTTPS traffic"
```

### [Пример настроек nftables](example-of-nftables-settings)

Пример настроек для командной строки (действуют до перезагрузки операционной системы):

```
sudo nft add table ip web_filter
sudo nft add chain ip web_filter input '{ type filter hook input priority 0; policy drop; sudo }'
sudo nft add rule ip web_filter input ip saddr 93.185.164.0/25 tcp dport {80, 443} accept
sudo nft add rule ip web_filter input tcp dport {80, 443} drop
```

Для постоянного применения нужно добавить следующие строки в файл `/etc/nftables.conf`:

```
table ip web_filter {
    chain input {
        type filter hook input priority 0; policy drop;
        ip saddr 93.185.164.0/25 tcp dport { 80, 443 } accept
    }
}
```

### [Пример настроек firewalld](example-of-firewalld-settings)

```
firewall-cmd --permanent --new-zone=ss
firewall-cmd --permanent --zone=ss --add-port=80/tcp
firewall-cmd --permanent --zone=ss --add-port=443/tcp
firewall-cmd --permanent --zone=ss --add-source=93.185.164.0/25
firewall-cmd --reload
```
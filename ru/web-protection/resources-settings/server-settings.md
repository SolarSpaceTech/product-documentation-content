---
id: 270
seoTitle: Дополнительные настройки сервера — Solar Space
seoDescription: Дополнительные настройки сервера — настройка веб-сервера Nginx, веб-сервера Apache, модуля mod_remoteip, настройка отображения реального IP-адреса в логах Apache, инструкция для BitrixVM 7 на CentOS, инструкция для IIS
displayName: Дополнительные настройки сервера
order: 6
published: true
historyName: Дополнительные настройки сервера
historyDescription: Информация по дополнительным настройкам сервера Solar Space
---

# [Дополнительные настройки сервера](additional-server-settings)

## [Настройка расшифровки реальных IP](setting-for-decryption-of-ip-addresses)

При проксировании трафика все запросы на ваш сервер поступают с IP-адресов сети Solar Space, а не с адресов реальных пользователей. Поэтому вы можете увидеть в логах IP-адрес 127.0.0.1. Чтобы сервер отображал реальные IP-адреса посетителей, необходимо настроить обработку заголовка X-Forwarded-For для сетей Solar Space:

* **93.185.164.0/25**

### [Веб-сервер Nginx](web-server-nginx)

Добавьте следующую строку в `/etc/nginx/nginx.conf` в секцию `http`:

```
http {
    ...
    set_real_ip_from 93.185.164.0/25;
    real_ip_header X-Forwarded-For;
    ...
}
```

Проверьте конфигурацию Nginx перед перезагрузкой:

```
sudo nginx -t
```

Перезагрузите Nginx:

```
sudo systemctl reload nginx
```

### [Веб-сервер Apache](web-server-apache)

Модуль `mod_rpaf` (устаревший вариант), лучше использовать `mod_remoteip`.

Создайте или измените файл `/etc/apache2/mods-enabled/rpaf.conf`, добавив следующие строки:

```
<IfModule mod_rpaf.c>
    RPAF_Enable On
    RPAF_SetHostName On
    RPAF_ProxyIPs 127.0.0.1 93.185.164.0
</IfModule>
```

Активируйте модуль `mod_rpaf` и конфигурацию:

```
sudo a2enmod rpaf
sudo a2enconf rpaf
```

Проверьте конфигурацию Apache перед перезагрузкой:

```
sudo apache2ctl -t
```

Перезагрузите Apache:

```
sudo systemctl reload apache2
```

### [Модуль mod_remoteip](module-mod-remoteip)

Если у вас ранее был установлен модуль `mod_rpaf`, деактивируйте его командой:

```
sudo a2dismod rpaf
```

Создайте или измените файл `/etc/apache2/conf-available/remoteip.conf`, добавив следующие строки:

```
<IfModule remoteip_module>
RemoteIPHeader X-Forwarded-For
RemoteIPTrustedProxy 127.0.0.1 93.185.164.0/25
</IfModule>
```

Активируйте модуль `mod_remoteip` и конфигурацию:

```
sudo a2enmod remoteip
sudo a2enconf remoteip
```

Проверьте конфигурацию Apache перед перезагрузкой:

```
sudo apache2ctl -t
```

Перезагрузите Apache:

```
sudo systemctl reload apache2
```

## [Настройка отображения реального IP-адреса в логах Apache](config-display-of-ip-address-in-apache-logs)

### [Инструкция для Ubuntu/Debian](instructions-for-ubuntu-debian)

Откройте файл `/etc/apache2/apache2.conf` и замените следующие строки:

```
LogFormat "%v:%p %h %l %u %t \"%r\" %>s %O \"%{Referer}i\" \"%{User-Agent}i\"" vhost_combined
LogFormat "%h %l %u %t \"%r\" %>s %O \"%{Referer}i\" \"%{User-Agent}i\"" combined
LogFormat "%h %l %u %t \"%r\" %>s %O" common
```

на:

```
LogFormat "%a:%p %h %l %u %t \"%r\" %>s %O \"%{Referer}i\" \"%{User-Agent}i\"" vhost_combined
LogFormat "%a %l %u %t \"%r\" %>s %O \"%{Referer}i\" \"%{User-Agent}i\"" combined
LogFormat "%a %l %u %t \"%r\" %>s %O" common
```

Проверьте конфигурацию Apache перед перезагрузкой:

```
sudo apache2 -t
```

Перезагрузите Apache:

```
sudo systemctl reload apache2
```

### [Инструкция для BitrixVM 7 на CentOS](instructions-for-bitrixvm-on-centos)

В BitrixVM 9 отображение реальных IP-адресов в логах Apache работает корректно по умолчанию, и дополнительных изменений не требуется.

Откройте файл `/etc/httpd/conf/httpd.conf` и найдите следующие строки:

```
LogFormat "%h %l %u %t \"%r\" %>s %b \"%{Referer}i\" \"%{User-Agent}i\"" combined
LogFormat "%h %l %u %t \"%r\" %>s %b" common
```

Замените символ `%h` на `%{X-Forwarded-For}i`, чтобы строки выглядели так:

```
LogFormat "%{X-Forwarded-For}i %l %u %t \"%r\" %>s %b \"%{Referer}i\" \"%{User-Agent}i\"" combined
LogFormat "%{X-Forwarded-For}i %l %u %t \"%r\" %>s %b" common
```

Сохраните изменения и закройте файл.

Проверьте конфигурацию Apache перед перезагрузкой:

```
sudo httpd -t
```

Перезагрузите Apache:

```
sudo systemctl reload httpd
```

### [Инструкция для IIS](instructions-for-iis)

Подробную инструкцию по настройке IIS вы можете прочитать [здесь](https://techcommunity.microsoft.com/blog/iis-support-blog/how-to-use-x-forwarded-for-header-to-log-actual-client-ip-address/873115[nofollow]).
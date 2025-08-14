---
id: 332
seoTitle: "Отправка сработок WAF в syslog"
seoDescription: "Пошаговая инструкция для администраторов по настройке передачи событий WAF из JSON-лога во внешний syslog-сервер с использованием rsyslog."
displayName: Интеграция
order: 55
published: true
tags: 
  - accent
  - quick start
---


# [Отправка сработок WAF в syslog](send-waf-events-to-syslog)

Этот раздел описывает, как настроить передачу событий WAF из JSON-лога во внешний syslog-сервер.

## [Установка rsyslog и модуля чтения файлов](install-rsyslog-and-imfile)

На серверах под управлением Ubuntu/Debian rsyslog установлен по умолчанию и умеет работать по UDP/TCP. Для чтения файлов используется модуль **imfile**, который входит в комплект и требует загрузки в конфигурации.

```bash
sudo apt update
sudo apt install rsyslog
```

## [Создание конфигурации для WAF JSON логов](create-config-for-waf-json-logs)

Создайте новый конфигурационный файл:

```bash
sudo nano /etc/rsyslog.d/30-waf-json.conf
```

Пример содержимого:

```bash
module(load="imfile")

input(
    type="imfile"
    File="/var/log/nginx/json_audit.json"
    Tag="waf-json:"
    Severity="info"
    Facility="local7"
)

if ($programname == 'waf-json') then {
    *.* @<ext_ip_address>:514
    stop
}
```

Для TCP вместо UDP используйте 

```bash
@@<ext_ip_address>:514
```



## [Перезапуск и проверка rsyslog](restart-and-check-rsyslog)

После внесения изменений перезапустите rsyslog и проверьте его статус:

```bash
sudo systemctl restart rsyslog
sudo systemctl status rsyslog
```

В выводе не должно быть ошибок.

---

Таким образом, события WAF из файла `/var/log/nginx/json_audit.json` будут передаваться на указанный внешний syslog-сервер по протоколу UDP (или TCP при соответствующей настройке).

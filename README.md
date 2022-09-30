# prometheus_install
Instruction for prometheus install

## Установка node_exporter

1) Скачать архив [c официального git](https://github.com/prometheus/node_exporter/releases/ "скачать prometheus") проекта версию для linux.
2) Распаковать его: ``tar xvfz node_exporter-*.*-amd64.tar.gz``
3) Зайти в каталог: ``cd node_exporter-*.*-amd64``
4) Переместить файл в /usr/bin: ``sudo cp node_exporter /usr/bin``

## Установка supervisor

1) ``sudo apt update && sudo apt install supervisor``
2) ``sudo systemctl status supervisor``
3) ``sudo nano /etc/supervisor/conf.d/idle.conf``
4) ``sudo nano /etc/supervisor/conf.d/prometheus_metrics.conf``

## Конфигурация supervisor

```
command=/usr/bin/node_exporter
autostart=true
autorestart=true
stderr_logfile=/var/log/node_exporter.err.log
stdout_logfile=/var/log/node_exporter.out.log
```
## Перезапуск демона supervisor

``sudo supervisorctl reread``

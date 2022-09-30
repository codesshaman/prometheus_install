# prometheus_install
Instruction for prometheus install

## Установка node_exporter

1) Скачать архив [c официального git](https://github.com/prometheus/node_exporter/releases/ "скачать prometheus") проекта версию для linux.
2) Распаковать его: ``tar xvfz node_exporter-*.*-amd64.tar.gz``
3) Зайти в каталог: ``cd node_exporter-*.*-amd64``
4) Переместить файл в /usr/bin: ``sudo cp node_exporter /usr/bin``

## Установка supervisor

1)

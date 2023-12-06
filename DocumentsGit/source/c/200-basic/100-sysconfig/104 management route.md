# {index}`management route`

## Назначение команды
Используйте эту команду для задания шлюза на коммутаторе для управления IP-адресом.

## Синтаксис команды
```
management route (add|del) gateway X.X.X.X
management route ipv6 (add|del) gateway X:X::X:X
```

| Параметр  | Описание параметра | Значение параметра |
|-----------|--------------------|---------------------|
| add       | Добавление маршрута | -                   |
| del       | Удаление маршрута   | -                   |
| ipv6      | Настройка шлюза IPv6 | -                   |
| gateway      | Добавить шлюз       | X.X.X.X (IPv4) или X:X::X:X (IPv6) |
| X.X.X.X | Адрес шлюза по умолчанию IPv4 | |
| X:X::X:X | Адрес шлюза по умолчанию IPv6 | |

## Командный режим
global config

## По умолчанию
Не указан

## Употребление
Никакой

## Примеры
```console
Switch# configure terminal
Switch(config)# management route add gateway 192.168.100.254
Switch(config)# management route ipv6 add gateway 2001:1000::1
```

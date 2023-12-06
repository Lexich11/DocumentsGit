# {index}`show management ip address`

## Назначение команды
Команда текущий IP-адрес, который назначен на интерфейс управления.

## Синтаксис команды
```
show management ip address
show management ipv6 address
```

## Командный режим
privileged exec 

## Примеры
```console
Switch# show management ip address
Management IP address is: 192.168.100.100/24
Gateway: 192.168.100.254
Switch# show management ipv6 address
Management IPv6 address is: 2001:1000::1000/96
Gateway: 2001:1000::1
```
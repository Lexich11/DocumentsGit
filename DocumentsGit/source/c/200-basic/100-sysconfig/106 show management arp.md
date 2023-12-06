# {index}`show management arp`

## Назначение команды
Команда выводит {term}`ARP` таблицу для интерфейса управления.

## Синтаксис команды
```
show management arp
```

## Командный режим
privileged exec

## Примеры
```console
Switch# show management arp
Address Hardware Addr Interface
----------------+--------------------+---------- 
10.10.39.241 00:11:12:13:14:c4 mgmt-if
10.10.39.254 00:11:12:13:14:6d mgmt-if
```
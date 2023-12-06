# {index}`management ip address`

## Назначение команды
Используйте эту команду для назначения IP-адреса на интерфейсе управления коммутатора. Для удаления IP-адреса используйте форму `no` этой команды.

## Синтаксис команды
```
management ip address ( X.X.X.X/M | X.X.X.X MASK ) ( gateway Y.Y.Y.Y/M | )
no management ip address
management ipv6 address ( X:X::X:X/M | X:X::X:X MASK ) ( gateway Y:Y::Y:Y | )
no management ipv6 address
```

| Параметр        | Описание | Возможные значения |
|-----------------|---------------------------------------------|---------------------------------|
| X.X.X.X/M       | {term}`IPv4`-адрес управления с длиной маски   | IPv4-адрес с длиной маски 1-32  |
| X.X.X.X MASK       | IPv4-адрес управления и маска   | IPv4-адрес и маска  |
| X:X::X:X/M      | {term}`IPv6`-адрес управления с длиной маски  | IPv6-адрес с длиной маски 1-128 |
| X:X::X:X MASK      | IPv6-адрес управления и маска  | IPv6-адрес и маска |
| gateway Y.Y.Y.Y    | Адрес шлюза по умолчанию IPv4                       | IPv4-адрес шлюза                |
| gateway Y:Y::Y:Y   | Адрес шлюза по умолчанию IPv6                       | IPv6-адрес шлюза                |

## Командный режим
global config

## По умолчанию
Не назначен. На интерфейсе управления включен клиент DHCP (для IPv4) и автоматическое получение адреса для IPv6.

## Употребление

## Примеры
```console
Switch# configure terminal
Switch(config)# management ip address 192.168.100.100/24
Switch(config)# no management ip address
Switch(config)# управление ipv6 адресом 2001:1000::1000/96
Switch(config)# no management ipv6 address
```
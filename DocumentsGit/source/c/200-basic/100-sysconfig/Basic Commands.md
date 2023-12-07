# {index}`hostname`

## Назначение команды
Для указания или изменения имени хоста на коммутаторе используйте команду `hostname` в глобальной конфигурации. Для восстановления значения по умолчанию используйте команду `no hostname`.

## Синтаксис команды
```
hostname NAME
no hostname
```

| Параметр | Описание параметра      | Значение параметра          |
|----------|-------------------------|-----------------------------|
| NAME     | Имя хоста для коммутатора | Строка (1-63 символа)       |

## Командный режим
global config

## По умолчанию
Имя хоста по умолчанию `Switch`.

## Употребление
Имя хоста используется в приглашениях и в именах файлов конфигурации. Имя должно соответствовать правилам ARPANET и содержать только буквы, цифры, дефисы и подчеркивание. Имена должны состоять из 64 символов или меньше.

## Примеры
```console
Switch# configure terminal
Switch(config)# hostname aquaswitch
aquaswitch(config)#
```
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
# {index}`show management interface`

## Назначение команды
Команда отображает конфигурацию, текущее состояние и статистику интерфейса управления.

## Синтаксис команды
```
show management interface
```

## Командный режим
privileged exec

## Примеры
```console
Switch# show management interface
Management Interface current state: DOWN
Description:
Link encap: Ethernet    HWaddr: 94:EB:AB:88:2A:B4
Inet addr: 192.168.100.102 Mask: 255.255.255.0
Bcast: 192.168.100.255 MTU: 1500
Speed: 10 Duplex: Half
Auto-negotiation: Enable
Received: 2 Packets, 128 Bytes (128.0 b)
Transmitted: 1 Packets, 78 Bytes (78.0 b
```

## Связанные команды
{ref}`clear counters mgmt-if`

# {index}`clear counters mgmt-if`

## Назначение команды
Команда сбрасывает накопленную статистику на интерфейсе управления.

## Синтаксис команды
```
clear counters mgmt-if
```

## Командный режим
privileged exec

## Примеры
```console
Switch# clear counters mgmt-if
```

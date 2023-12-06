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
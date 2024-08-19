# LINUX serial connection

```shell
dnf install statserial, screen -y

OPTIONAL

dnf install putty -y

OPTIONAL

dnf install minicom
#powerfull tool for serial connections

```

```shell
$> dmesg
...
..
.
[ 3028.342451] usb 1-1: new full-speed USB device number 9 using xhci_hcd
[ 3028.470083] usb 1-1: New USB device found, idVendor=067b, idProduct=2303, bcdDevice= 3.00
[ 3028.470099] usb 1-1: New USB device strings: Mfr=1, Product=2, SerialNumber=0
[ 3028.470105] usb 1-1: Product: USB-Serial Controller
[ 3028.470111] usb 1-1: Manufacturer: Prolific Technology Inc.
[ 3028.472340] pl2303 1-1:1.0: pl2303 converter detected
[ 3028.473408] usb 1-1: pl2303 converter now attached to ttyUSB0
.
..
...

```


We have to define which dev will be our USB/SERIAL converter will be installed - in this case: `ttyUSB0`

Now we can check serial pin status:
```shell
$> statserial /dev/ttyUSB0

Device: /dev/ttyUSB0

Signal  Pin  Pin  Direction  Status  Full
Name    (25) (9)  (computer)         Name
-----   ---  ---  ---------  ------  -----
FG	 1    -      -           -   Frame Ground
TxD	 2    3      out         -   Transmit Data
RxD	 3    2      in          -   Receive  Data
RTS	 4    7      out         1   Request To Send
CTS	 5    8      in          0   Clear To Send
DSR	 6    6      in          0   Data Set Ready
GND	 7    5      -           -   Signal Ground
DCD	 8    1      in          0   Data Carrier Detect
DTR 20    4      out         1   Data Terminal Ready
RI	22    9      in          0   Ring Indicator
```

To run serial in screen

```shell
screen /dev/ttyUSB0 38400
```


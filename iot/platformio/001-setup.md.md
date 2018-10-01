# Install PlatformIO Core (CLI)
## Install virtualenv


```bash
sudo apt install virtualenv
```
## Install PlatformIO Core

Follow the instructions provided on [https://docs.platformio.org/en/latest/installation.html#virtual-environment](https://docs.platformio.org/en/latest/installation.html#virtual-environment)

## Activate PlatformIO Core

```bash
source ~/Kode/virtualenv/pio/bin/activate
```

## Prepare system
It might be possible that it is needed to add the current user to a group which has access to the FTDI USB Adapter device handler. After connecting the adapter via usb ``dmesg`` should return something similar to

```log
[ 1043.094445] usb 1-1: new full-speed USB device number 5 using xhci_hcd
[ 1043.249288] usb 1-1: New USB device found, idVendor=0403, idProduct=6015
[ 1043.249294] usb 1-1: New USB device strings: Mfr=1, Product=2, SerialNumber=3
[ 1043.249298] usb 1-1: Product: FT231X USB UART
[ 1043.249303] usb 1-1: Manufacturer: FTDI
[ 1043.249306] usb 1-1: SerialNumber: DJ008CP1
[ 1043.309452] usbcore: registered new interface driver usbserial_generic
[ 1043.309466] usbserial: USB Serial support registered for generic
[ 1043.313145] usbcore: registered new interface driver ftdi_sio
[ 1043.313166] usbserial: USB Serial support registered for FTDI USB Serial Device
[ 1043.313274] ftdi_sio 1-1:1.0: FTDI USB Serial Device converter detected
[ 1043.313323] usb 1-1: Detected FT-X
[ 1043.313589] usb 1-1: FTDI USB Serial Device converter now attached to ttyUSB0
```
Checking for the permissions of ``/dev/ttyUSB0``:
```bash
> ls -la /dev/ttyUSB0
crw-rw---- 1 root dialout 188, 0 Okt  1 19:32 /dev/ttyUSB0
```

Add the user to ``dialout`` group:
```bash
sudo adduser me dialout
```
Finally re-login to enable all changes or open a login shell.
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTIwMzIxNjkxMzgsLTQwMzY1OTQ2MF19
-->
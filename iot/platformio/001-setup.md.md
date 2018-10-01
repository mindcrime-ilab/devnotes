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

```
```
> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTgyMzY5MzMyOSwtNDAzNjU5NDYwXX0=
-->
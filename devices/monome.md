#Udev rule

```bash
SUBSYSTEM=="usb", ENV{DEVTYPE}=="usb_device", ATTRS{idVendor}=="0403", ATTRS{idProduct}=="6001", TAG+="uaccess", PROGRAM="/bin/sh -c 'echo -n $id:1.0 >/sys/bus/usb/drivers/ftdi_sio/unbind'"
```

or install `libftdi`

# Propose 

This is a example showing how to use the Pico-PIO-USB library


## links
* [library](https://github.com/sekigon-gonnoc/Pico-PIO-USB)
* [Host and device example](https://github.com/sekigon-gonnoc/Pico-PIO-USB/tree/main/examples/host_hid_to_device_cdc)
* [USB device](https://github.com/hathach/tinyusb/tree/master/examples/device/hid_composite)


# program board

```bash
mkdir build
cd build
make -j8
openocd -f interface/cmsis-dap.cfg -c "adapter speed 5000" -f target/rp2040.cfg -c "program USB_DEVICE_AND_KEYBOARD.elf verify reset exit"
```

# mac
ls /dev/tty.usb*

screen /dev/tty.usbmodem1234567890121
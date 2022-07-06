I2C-CH341-USB Linux kernel driver
=================
CH341 to i2c bus linux kernel driver. With this driver inserted to Linux kernel, you can write your code using the standard Linux I2C API.
## How to use it
```
make
insmod i2c-ch341-usb.ko i2c_speed=1
```
## Kernel Module Parameters
```
parm:           i2c_speed:I2C Bus Speed. 0 = 20kHz, 1 = 100kHz, 2 = 400kHz, 3 = 750kHz (uint)
```

I2C-CH341-USB Linux kernel driver
=================
CH341 to i2c bus linux kernel driver. With this driver inserted to Linux kernel, you can write your code using the standard Linux I2C API.
## How to compile and load
```
make
sudo make install
sudo modprobe i2c-ch341-usb i2c_speed=1
```
## How to unload
```
sudo rmmod i2c-ch341-usb
```

## Kernel Module Parameters
```
parm:           i2c_speed:I2C Bus Speed. 0 = 20kHz, 1 = 100kHz, 2 = 400kHz, 3 = 750kHz (uint)
```

## Using Linux I2C Utils

Using the package i2c-utils, you can perform an I2C scan

```
$ sudo i2cdetect -y 11
     0  1  2  3  4  5  6  7  8  9  a  b  c  d  e  f
00:                         -- -- -- -- -- -- -- -- 
10: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
20: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
30: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
40: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
50: 50 -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
60: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- 
70: -- -- -- -- -- -- -- --          
```

Here you can see, that a device was found at I2C Address 0x50.

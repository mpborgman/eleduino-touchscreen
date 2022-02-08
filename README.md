# eleduino-touchscreen
Eleduino touchscreen DKMS driver
Reworked from old waveshare driver.

Mille grazie to https://github.com/110yd !!

This driver can also be used for Raspberry Pi on Eleduino 7 inch screen, with a small mod in `wsh7tsc.c`.

```
#define WSH7INCH_WIDTH                  1024
#define WSH7INCH_HEIGHT                 600
```

I didn't change var and const names, as it was of no additional value to me.

### Compile:
1. Install dkms and raspberrypi-kernel-headers

```
sudo apt-get install dkms raspberrypi-kernel-headers
```

2. Extract source folder into`/usr/src/wsh7inch-0.1/`

3. Build through DKMS system:

```
sudo dkms build wsh7inch/0.1
```

### Install

```
sudo dkms install wsh7inch/0.1
```
### Restrictions

* Sometimes touchscreen is really buggy. This driver does not perform any data correction

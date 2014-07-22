## New i2c(8)

This is correction for i2c(8) utility in FreeBSD to work on Raspberry Pi

* i2c.c.patch - this is a patch for original source code of the i2c.c
* newi2c.c - this is an updated source code of the i2c.c

## Comments to this patch from the FreeBSD team:

* unfortunately this patch is doing some evil stuff to make the search work
* It can also lock up the bus and/or devices while scanning the bus (you need to write at least two bytes or some devices will be left in an unknown state at the end of scanning)
 
https://bugs.freebsd.org/bugzilla/show_bug.cgi?id=189914

## Use this patch at your own risk

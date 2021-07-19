*************************************************************
*                                                           			            *
*                                                           			            *
*                  How to setup the driver                  		            *
*                                                           			            *
*                                                           			            *
*************************************************************

Files description:

1. kernel
   /drivers/    SiS I2C Touchscreen drvier source code.
   /Makefile    The Makefile under kernel
   /config_sis  The config file for Beagleboard.




How to make kernel:

1. Patch the Touchscreen driver to your kernel. The source codes are in the "kernel" folder.


2. Select feature of the I2C touchscreen driver in menuconfig.

   $ make menuconfig
     [*]Device Drivers --> Input device support --> Touchscreens --> SiS 81x family I2C touchscreen driver

3. In drivers/input/touchscreen/sis_i2c.h
    The X, Y sensing lines is defined in 
    #define X_SENSE_LINE		38
    #define Y_SENSE_LINE		22

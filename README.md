# pi_zero_w_buildroot
Buildroot configuration for Pi Zero W that enables WiFi and Bluetooth on startup

To use, copy the entire directory "pi_zero_w" into the Buildroot "board" folder. Copy the file "pi_zero_w_defconfig into the Buildroot "configs" folder.

Run "make pi_zero_w_defconfig"

If you need to make changes to the configuration run "make menuconfig"

Run "make" to build the OS. There are rootfs overlay files that replace /etc/profile and /etc/inittab. The module loading is done from /etc/profile when you login ("root").  You will need to change the info in wpa_supplicant.conf for your wifi network.

You can get the wlan0 address using "ip addr" from the commandline.

You can setup Bluetooth using "bluetoothctl" from the commandline.





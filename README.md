# OWASP_IOTgoat_build_for_A5-V11_mini_3G_router


This repo has been made in regard to an issue with the OWASP IOTgoat project

https://github.com/OWASP/IoTGoat

The IoTGoat Project is a deliberately insecure firmware based on OpenWrt and maintained by OWASP as a platform to educate software developers and security professionals with testing commonly found vulnerabilities in IoT devices.

The IOTgoat project offer some pre-made binaries for Raspberry Pi 2 and X86 machines. Additionally, a VMDK image to use with VMware/VBox and virtualization with Qemu.

However, Internet Of Things (IOT) devices are non-standard computing "hardware". 
IOT devices in essence are gadgets that connect wirelessly to a network and can transmit data. IOT devices most times are small and inexpensive.
Therefore, is not a better experience to run 'the vulnearable IOTgoat firmware' in a real IOT device?

Enter the A5-V11 mini router 
https://openwrt.org/toh/unbranded/a5-v11


# Steps to install the IOTgoat binary into A5-V11 mini 3G router

1. Install a base OpenWRT firmware. For this purpose please follow the steps on the OpenWRT site https://openwrt.org/toh/unbranded/a5-v11#first-time_installation
   Once the OpenWRT installation its done come back here.
   
2. Following the 10 steps on that page you need to install:
   
   - A new Uboot image, from this site:
     https://disk.yandex.com/d/ubSsjNZU34Xk2L  download the image called Uboot_usb_256_03.img
     Please, be careful ins this section following the steps to install the 'Uboot image', this part is super important as it will determine if you can continue with the process or simple place your device in the garbage bin.
   - A OpenWRT factory firmware, from here:
     https://archive.openwrt.org/chaos_calmer/15.05.1/ramips/rt305x/openwrt-15.05.1-ramips-rt305x-a5-v11-squashfs-factory.bin

4. Now, connect to your device openning your browser at 192.168.1.1, then go under 'system' > Firmware upgrade and there, install the sysupgrade image for the A5-v11 device, get it from here:
   https://archive.openwrt.org/chaos_calmer/15.05.1/ramips/rt305x/openwrt-15.05.1-ramips-rt305x-a5-v11-squashfs-sysupgrade.bin
   
5. Now, once again connect to your device openning your browser at 192.168.1.1, then go under 'system' > Firmware upgrade and there, this time  you will install the IOTgoat firmware made for the A5-V11 mini router.

6. The custom binary is located in the release section of this page, donwload it and install it to your device. After upgrading, your IOTgoat would be ready to be hacked.

7.  Done. Drink beer!
          

# PS. TRICK TO RECOVER. In case of failure or your device is no being accessible.

1.-Get a USB flash drive formated to FAT32
2.-Place the OpenWRT sysupgrade image (from step 4) on the root directory of the USB flash drive
3.-Connect the USB to your device
4. While holding the reset button, power the device. (keep holding the reset button for 10 seconds, the release the button)
5. Your USB flash drive will light up and the sysupgrade image will be installed to your device.
6. Now, you are back in bussines. Install the IOTgoat image again and keep hacking. 
Now you know why being careful installing the Uboot image was super important.
7. Get another beer!






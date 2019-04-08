# hikey970
binary files for the hikey 970 such as kernel and modules.

## kernelmodules.tgz

the modules belong in the directory /lib/modules

```
sudo tar xvzf kernelmodules.tgz -C /lib/modules/
```


## grub.cfg

Be aware that grub.cfg is configured for my setup. only use as an example on how to configure.
Do NOT use it as-is, your board may not boot with it.

Specifically of interest is the part:

```
drm.debug=0xf drm_kms_helper.edid_firmware=edid/1920x1080.bin video=HDMI-A-1:1920x1080@60e consoleblank=0
```

This is added to force the kernel to use a specific edid and force the resolution to 1920x1080.

## /boot directory:

```
janrinze@hikey970:/boot$ ls -al                      
total 22536
drwxrwxrwx  5 root     root         4096 Apr  7 21:06 .
drwxr-xr-x 23 root     root         4096 Jun  8  2018 ..
drwxrwxrwx  3 root     root         4096 Feb 13  2018 EFI
-rw-r--r--  1 janrinze janrinze 22979072 Apr  7 20:55 Image
drwxrwxrwx  2 root     root         4096 Apr  7 21:04 grub
-rw-r--r--  1 janrinze janrinze    69205 Apr  7 20:50 kirin970-hikey970.dtb
drwxr-xr-x  2 root     root         4096 Apr  7 21:06 old
janrinze@hikey970:/boot$ ls -al grub
total 12
drwxrwxrwx 2 root root 4096 Apr  7 21:04 .
drwxrwxrwx 5 root root 4096 Apr  7 21:06 ..
-rwxrw-rw- 1 root root 1323 Apr  7 21:04 grub.cfg
janrinze@hikey970:/boot$ ls -al EFI/BOOT/
total 40
drwxrwxrwx 2 root root  4096 Feb 13  2018 .
drwxrwxrwx 3 root root  4096 Feb 13  2018 ..
-rwxrw-rw- 1 root root 28960 Feb 13  2018 fastboot.efi
janrinze@hikey970:/boot$ 
```


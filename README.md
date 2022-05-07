# RE_NOTE-BOOK
Reverse engineering notes and books

# move certificate to system dir
```
adb root
adb disable-verity
adb reboot
adb root
adb remount
adb shell
mount -o rw,remount /system
ls -al /data/misc/user/0/cacerts-added/ #查看有那些用户证书
cp /data/misc/user/0/cacerts-added/* /etc/security/cacerts/ #把安装的用户证书全部复制到系统目录
mount -o ro,remount /system
```

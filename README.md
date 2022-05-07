# RE_NOTE-BOOK
Reverse engineering notes and books

# move certificate to system dir
```
adb root<br> 
adb disable-verity<br> 
adb reboot<br> 
adb root<br> 
adb remount<br> 
adb shell<br> 
mount -o rw,remount /system<br> 
ls -al /data/misc/user/0/cacerts-added/ #查看有那些用户证书<br> 
cp /data/misc/user/0/cacerts-added/* /etc/security/cacerts/ #把安装的用户证书全部复制到系统目录<br> 
mount -o ro,remount /system<br> 
```

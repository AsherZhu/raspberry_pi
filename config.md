# Raspberry pi

### Install 

> ? 2015-02-16-raspbian-wheezy.img

> PI3 b+: 2017-04-10-raspbian-jessie.img

> [images download](http://downloads.raspberrypi.org/raspbian/images/)

1. erase SD card
2. df -h
3. diskutil unmount /dev/your_sd_disk
4. diskutil list
5. sudo dd bs=4m if=path_to_your_image.img of=/dev/your_sd_disk
6. diskutil unmountDisk /dev/your_sd_disk

### Wifi configuration

> [有線或無線的 DHCP 設定或固定 IP 設定](https://sites.google.com/site/raspberypishare0918/home/di-yi-ci-qi-dong/1-6-you-xian-huo-wu-xian-dedhcp)

```
sudo nano /etc/network/interfaces
```

```
auto lo eth0
iface lo inet loopback

#iface eth0 inet dhcp
#iface wlan0 inet manual
allow-hotplug wlan0
auto wlan0
#iface wlan0 inet manual 
#wpa-roam /etc/wpa_supplicant/wpa_supplicant.conf 
iface wlan0 inet static 
address 192.168.31.99 
netmask 255.255.255.0 
gateway 192.168.31.1 
wpa-ssid BIG_DATA 
wpa-psk 17021703
wireless-power off
iface default inet dhcp
```

```
sudo nano /etc/kbd/config 
```

```
BLANK_TIME=0 
POWERDOWN_TIME=0 
```
```
sudo reboot
```

### JDK `jessie already installed JDK8`

```
sudo apt-get update && sudo apt-upgrade
sudo apt-get install oracle-java8-jdk
```

### MySQL

```
sudo apt-get update && sudo apt-get upgrade
sudo apt-get install mysql-server
```

### Tomcat

```
http://mirror.jax.hugeserver.com/apache/tomcat/tomcat-7/v7.0.76/bin/apache-tomcat-7.0.76.tar.gz
tar xvf apache-tomcat-7.0.76.tar.gz
cd apache-tomcat-7.0.76/bin
./startup.sh
```
    
### Common command
1. sudo raspi-config
2. sudo reboot
3. ifconfig
4. nano    

### Common Errors
1. No space left on device

```
sudo raspi-config
Expend Filesystem
Ok
Yes
df -h
```

2. Chinese settings

```
sudo raspi-config	
「Internationalisation Options」
「Change Locale」
「zh_CN.UTF-8 UTF-8」
「en_US.UTF-8」

install Chinese fonts
sudo apt-get update
sudo apt-get install ttf-wqy-microhei ttf-wqy-zenhei xfonts-wqy
sudo apt-get install fcitx
```
		
3. telnet

```
luit -encoding GB2312 telnet bbs.zixia.net
```

### MISC
1. Edit login welcome message
```
sudo nano /etc/motd
```

```		
sudo nano /etc/ssh/sshd_config
PrintLastLog=no
sudo /etc/init.d/ssh restart	
```
		
2. HDMI with projector

	Edit boot/config.txt,uncomment lines.`not worked`

	```
	hdmi_safe= 
	overscan_left= 
	overscan_right= 
	overscan_top= 
	overscan_bottom= 
	hdmi_group= 
	hdmi_mode= 
	hdmi_drive= 
	config_hdmi_boost= 
	```
	

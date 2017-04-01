# How to Check the Software and Hardware Version of a Raspberry Pi

> [How to Check the Software and Hardware Version of a Raspberry Pi](http://ozzmaker.com/check-raspberry-software-hardware-version-command-line/)

There are a number of commands which can be used to check the hardware and software versions on a Raspberry Pi.

### Version of Debian;

> cat /etc/debian_version can be used to see what version of Debian you are running.

    pi@raspberrypi ~ $ cat /etc/debian_version
    7.8
    2015-05-05-raspbian-wheezy

    pi@raspberrypi ~ $ cat /etc/debian_version
    8.0
    2016-02-03-raspbian-jessie

### OS Release Notes;

> cat /etc/os-release can be used to see OS release notes

    pi@raspberrypi ~ $ cat /etc/os-release
    PRETTY_NAME=”Raspbian GNU/Linux 7 (wheezy)”
    NAME=”Raspbian GNU/Linux”
    VERSION_ID=”7″
    VERSION=”7 (wheezy)”
    ID=raspbian
    ID_LIKE=debian
    ANSI_COLOR=”1;31″
    HOME_URL=”http://www.raspbian.org/”
    SUPPORT_URL=”http://www.raspbian.org/RaspbianForums”
    BUG_REPORT_URL=”http://www.raspbian.org/RaspbianBugs”
    2015-05-05-raspbian-wheezy

    pi@raspberrypi ~ $ cat /etc/os-release
    PRETTY_NAME=”Raspbian GNU/Linux 8 (jessie)”
    NAME=”Raspbian GNU/Linux”
    VERSION_ID=”8″
    VERSION=”8 (jessie)”
    ID=raspbian
    ID_LIKE=debian
    HOME_URL=”http://www.raspbian.org/”
    SUPPORT_URL=”http://www.raspbian.org/RaspbianForums”
    BUG_REPORT_URL=”http://www.raspbian.org/RaspbianBugs”
    2016-02-03-raspbian-jessie

### Kernel Version;

> uname -a can be used to see what kernel version is running

    pi@raspberrypi ~ $ uname -a
    Linux raspberrypi 3.18.11-v7+ #781 SMP PREEMPT Tue Apr 21 18:07:59 BST 2015 armv7l GNU/Linux
    2015-05-05-raspbian-wheezy

    pi@raspberrypi ~ $ uname -a
    Linux raspberrypi 4.1.19-v7+ #858 SMP Tue Mar 15 15:56:00 GMT 2016 armv7l GNU/Linux
    2016-02-03-raspbian-jessie

 

### BerryIMU Raspberry Pi Gyroscope Accelerometer

> cat /proc/cpuinfo can be used to see what hardware you are using. Take note of the revision number in **the second last line** and then refer to the table below. The output below is from a Pi 2

    pi@raspberrypi ~ $ cat /proc/cpuinfo
    processor : 0
    model name : ARMv7 Processor rev 5 (v7l)
    BogoMIPS : 38.40
    Features : half thumb fastmult vfp edsp neon vfpv3 tls vfpv4 idiva idivt vfpd32 lpae evtstrm
    CPU implementer : 0x41
    CPU architecture: 7
    CPU variant : 0x0
    CPU part : 0xc07
    CPU revision : 5processor : 1
    model name : ARMv7 Processor rev 5 (v7l)
    BogoMIPS : 38.40
    Features : half thumb fastmult vfp edsp neon vfpv3 tls vfpv4 idiva idivt vfpd32 lpae evtstrm
    CPU implementer : 0x41
    CPU architecture: 7
    CPU variant : 0x0
    CPU part : 0xc07
    CPU revision : 5processor : 2
    model name : ARMv7 Processor rev 5 (v7l)
    BogoMIPS : 38.40
    Features : half thumb fastmult vfp edsp neon vfpv3 tls vfpv4 idiva idivt vfpd32 lpae evtstrm
    CPU implementer : 0x41
    CPU architecture: 7
    CPU variant : 0x0
    CPU part : 0xc07
    CPU revision : 5processor : 3
    model name : ARMv7 Processor rev 5 (v7l)
    BogoMIPS : 38.40
    Features : half thumb fastmult vfp edsp neon vfpv3 tls vfpv4 idiva idivt vfpd32 lpae evtstrm
    CPU implementer : 0x41
    CPU architecture: 7
    CPU variant : 0x0
    CPU part : 0xc07
    CPU revision : 5Hardware : BCM2709
    Revision : a21041
    Serial : 00000000c15e9432
    pi@raspberrypi ~ $

|MODEL AND PI REVISION	|256MB|	HARDWARE REVISION CODE FROM CPUINFO|
|---|---|---|
|Model B Revision 1.0	|256MB|	0002|
|Model B Revision 1.0 + ECN0001 (no fuses, D14 removed)	|256MB|	0003|
|Model B Revision 2.0<br>Mounting holes	|256MB|	0004<br>0005<br>0006|
|Model A<br>Mounting holes	|256MB|	0007<br>0008<br>0009|
|Model B Revision 2.0<br>Mounting holes	|512MB|	000d<br>000e<br>000f|
|Model B+	|512MB|	0010|
|Compute Module	|512MB|	0011|
|Model A+	|256MB|	0012|
|Pi 2 Model B	|1GB|	a01041 (Sony, UK)<br>a21041 (Embest, China)|
|PiZero	|512MB|	900092(no camera connector)<br>900093(camera connector)|
|Pi 3 Model B	|1GB|	a02082 (Sony, UK)<br>a22082 (Embest, China)|

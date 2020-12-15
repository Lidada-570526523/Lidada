# Lidada
关于Android Studio打开无限报错的解决方案
关于Android Studio启动虚拟机后无限报错的解决方法：

log：

Hax is enabled
Hax ram_size 0x40000000
HAX is working and emulator runs in fast virt mode.
audio: Failed to create voice `goldfish_audio_in'
qemu-system-i386.exe: warning: opening audio input failed
emulator: Listening for console connections on port: 5554
emulator: Serial number of this emulator (for ADB): emulator-5554
VCPU shutdown request
EAX=00748cea EBX=3ffadb60 ECX=00000000 EDX=00000000
ESI=00000000 EDI=00000000 EBP=00000000 ESP=00006d38
EIP=3ffb6921 EFL=00010082 [--S----] CPL=0 II=0 A20=1 SMM=0 HLT=0
VCPU shutdown request
ES =0010 00000000 ffffffff 00c09300 DPL=0 DS  [-WA]
VCPU shutdown request
CS =0008 00000000 ffffffff 00c09b00 DPL=0 CS32 [-RA]
VCPU shutdown request
SS =0010 00000000 ffffffff 00c09300 DPL=0 DS  [-WA]
VCPU shutdown request
DS =0010 00000000 ffffffff 00c09300 DPL=0 DS  [-WA]
VCPU shutdown request
VCPU shutdown request
FS =0010 00000000 ffffffff 00c09300 DPL=0 DS  [-WA]
GS =0010 00000000 ffffffff 00c09300 DPL=0 DS  [-WA]
VCPU shutdown request
LDT=0000 00000000 0000ffff 00008200 DPL=0 LDT
TR =0000 00000000 0000ffff 00008b00 DPL=0 TSS32-busy
GDT=   000f6be8 00000037









原因：第七代cup的问题。

解决方案：将安卓SDK\extras\intel\Hardware_Accelerated_Execution_Manager文件夹备份后将其包含的文件删除-->将Hmax_6.0.5解压文件夹里面的所有文件剪切到Hardware_Accelerated_Execution_Manager文件夹下-->点击其中的intelhaxm-android.exe-->启动安装向导，覆盖先前安装的hmax-->安装完成以后，打开AS，新建模拟器，就能正常运行了！

 

百度云盘分享HMAX_6.0.5： http://pan.baidu.com/s/1geFFoRL

​                       https://pan.baidu.com/s/1CENhwu-ZySD0vL5DH0gRjg

微软官网下载地址:https://software.intel.com/en-us/articles/intel-hardware-accelerated-execution-manager-intel-haxm

 CSDN HMAX资源下载：https://download.csdn.net/download/nsongbai/10866751

​                    https://download.csdn.net/download/nsongbai/10866770

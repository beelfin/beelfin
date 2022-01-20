# resize hd
잘 안됨. 이거 하고 VM 죽어서 재 설치함.
```
VBoxManage modifyhd --resize 20000 "/Users/scott/VirtualBox VMs/ubuntu20.04/ubuntu20.04.vdi"
```

# VM resolution 
```
I fixed the problem by doing:

Turn off 3D Acceleration in the VB settings -- that's why the Guest Additions were locking up after login.
Run this in the terminal of your ubuntu virtual machine, not the host OS:

apt-get update  
apt-get upgrade  
apt-get install dkms  
apt-get install build-essential
Go to the Devices menu and tell it to install the Guest Additions. A new CDROM will appear on the desktop. Rightclick and choose the Autorun.
Restart the VM.
Now resize the VM window or choose Full Screen mode and it will resize the desktop screen resolution properly.
```

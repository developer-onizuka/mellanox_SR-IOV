# mellanox_SR-IOV

```

 1028  sudo mount -t ext4 -o data=ordered /dev/nvme0n1 /mnt
 1029  lspci -nnn 
 1030  lspci -nnk -d 15b3:1003
 1031  lspci -nnk -d 10de:1cb1
 1032  lsmod |grep mlx4
 1033  rmmod mlx4_core
 1034  sudo rmmod mlx4_core
 1035  lsmod |grep mlx4
 1036  lspci -nnk -d 15b3:1003
 1037  dpkg -l |grep mlx
 1038  sudo vi /etc/modprobe.d/mlnx.conf
 1039  reboot
 1040  lsmod |grep mlx
 1041  sudo vi /etc/modprobe.d/mlnx.conf
 
 $ cat /etc/modprobe.d/mlnx.conf 
blacklist mlx4_core


 1042  sudo update-initramfs -u
 1043  reboot
 1044  lsmod |grep mlx

```


```
$ cd mlnx-en-5.0-1.0.0.0-ubuntu20.04-x86_64/
$ sudo ./install 
Logs dir: /tmp/mlnx-en.2172.logs
General log file: /tmp/mlnx-en.2172.logs/general.log

Below is the list of mlnx-en packages that you have chosen
(some may have been added by the installer due to package dependencies):

ofed-scripts
mlnx-en-utils
mlnx-en-dkms
mstflint

This program will install the mlnx-en package on your machine.
Note that all other Mellanox, OEM, OFED, RDMA or Distribution IB packages will be removed.
Those packages are removed due to conflicts with mlnx-en, do not reinstall them.

Do you want to continue?[y/N]:y

Checking SW Requirements...
Removing old packages...
Installing new packages
Installing ofed-scripts-5.0...
Installing mlnx-en-utils-5.0...
Installing mlnx-en-dkms-5.0...
Installing mstflint-4.13.0...
Selecting previously unselected package mlnx-fw-updater.
(Reading database ... 251723 files and directories currently installed.)
Preparing to unpack .../mlnx-fw-updater_5.0-1.0.0.0_amd64.deb ...
Unpacking mlnx-fw-updater (5.0-1.0.0.0) ...
Setting up mlnx-fw-updater (5.0-1.0.0.0) ...
Attempting to perform Firmware update...
Querying Mellanox devices firmware ...

Device #1:
----------

  Device Type:      ConnectX3
  Part Number:      MCX311A-XCA_Ax
  Description:      ConnectX-3 EN network interface card; 10GigE; single-port SFP+; PCIe3.0 x4 8GT/s; RoHS R6
  PSID:             MT_1170110023
  PCI Device Name:  03:00.0
  Port1 MAC:        f4521488d550
  Port2 MAC:        f4521488d551
  Versions:         Current        Available     
     FW             2.33.5220      2.42.5000     
     PXE            3.4.0467       3.4.0752      

  Status:           Update required

---------
Found 1 device(s) requiring firmware update...

Device #1: Updating FW ...     
Done

Restart needed for updates to take effect.
Log File: /tmp/mlnx-en.2172.logs/fw_update.log
Device (03:00.0):
	03:00.0 Ethernet controller: Mellanox Technologies MT27500 Family [ConnectX-3]
	Link Width: x4
	PCI Link Speed: 8GT/s

Installation passed successfully
To load the new driver, run:
/etc/init.d/mlnx-en.d restart
```

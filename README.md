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

If the current user does not have access to the mounted shared folders, add user to vboxsf group 
```
sudo adduser $USER vboxsf
```

Mount vdi disk
```
sudo apt-get install qemu-kvm
sudo modproble nbd
qemu-nbd -c /dev/nbd0 /home/user/VMs/vm.vdi
sudo fdisk -l /dev/nbd0
sudo mount /dev/nbd0p1 /mnt
```

After install guest additions
```
sudo apt-get install build-essential linux-headers-`uname -r` dkms
```

Right Ctrl + F1 to send Ctrl-Alt-F1 to the linux host

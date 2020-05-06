Reference:
► https://wiki.archlinux.org/index.php/KVM - KVM
► https://wiki.archlinux.org/index.php/QEMU - QEMU
► https://wiki.archlinux.org/index.php/Libvirt - Libvirt
► https://virt-manager.org/ - Virt-manager
► https://wiki.archlinux.org/index.php/Polkit - Polkit

► https://computingforgeeks.com/use-virt-manager-as-non-root-user/


```
LC_ALL=C lscpu | grep Virtualization
sudo pacman -S lxsession
sudo pacman -S qemu virt-manager ebtables
sudo systemctl enable libvirtd
sudo systemctl start libvirtd
sudo systemctl status libvirtd
sudo usermod -G libvirt -a subhash

// if required
sudo pacman -S dnsmasq

// if NAT is inactive
sudo virsh net-list --all
sudo virsh net-start default
sudo virsh net-autostart default
```

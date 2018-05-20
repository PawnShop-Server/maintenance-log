# PawnShop
## Server Upgrade
__Start Date:__ 5/19/2018
__End Date:__ _On-going_
__Start Time:__ 4:00 PM
__End Time:__ _On-going_

### Pre-Blackout
- [ ] ~~Migrate VMs. Run `virsh dumpxml $vm > $vm.xml`~~ Ubuntu is corrupted.
aborting.
- [x] Backup Samba configurations
- [x] Migrate LVMs. Unmount all volumes, then run
```
sudo vgchange -an pawnshop_main_array
sudo vgexport pawnshop_main_array
```
- [x] Backup boot drive. Run `sudo -i` and `pv < /dev/sda > /dev/sdd`

### Blackout Phase 1
- [x] Clean fans
- [x] Clean heatsink (optional)
- [x] Replace thermal paste (optional)
- [x] Replace boot hard drive
- [x] Set boot controller to `SATA Mass Storage`
- [x] Install Ubuntu Server 18.04 LTS
- [x] Activate LVM
- [x] Expand LVM. First add the new drive to a one-disk RAID0 array. Then, add
that array into the LVM array.

### Checkpoint #1
- [ ] Backup boot drive

### Blackout Phase 2
- [ ] Configure libvirt and KVM
- [ ] Activate VMs

### Checkpoint #2
- [ ] Backup boot drive

### Blackout Phase 3
- [ ] Install Samba and Winbind
- [ ] Configure and activate Samba

### Checkpoint #3
- [ ] Backup boot drive

### Post-Blackout
- [ ] Notify _Trusted Three_; email to `trustedthree@thenwhatstudios.com`

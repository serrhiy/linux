
1. ```fdisk``` - manipulate disk partition table:
  a. ```fdisk -l``` - list the partition tables for the specified devices;
  b. ```fdisk -l <device>```;
  c. ```fdisk <device>``` - move to device settings;
2. ```lvm``` - LVM2 tools;
3. ```pvscan``` - list all physical volumes;
4. ```pvcreate``` - create physical volume;
5. ```vgscan``` - search for all volume groups;
6. ```vgcreate``` - create volume group:
  a. ```vgcreate <vgname> <volumenames>```;
7. ```lvscan``` - list all logical volumes in all volume groups;
8. ```lvcreate``` - create a logical volume;
9. ```lvdisplay``` - Display information about a logical volume;
10. ```lvextend``` - add space to a logical volume;
11. ```lsblk``` - list block devices;
12. ```mkfs``` - build a Linux filesystem:
  a. ```mkfs -t ext2 <device>```;
13. ```mkswap``` - set up a Linux swap area;
14. ```swapon, swapoff``` - enable/disable devices and files for paging and swapping;
15. ```umount``` - unmount filesystems;
<h1 align="center"> Storage </h1>

### Disk Partitions

+ lsblk - list the block device
+ ls -l | grep ^b - list the block devices
+ sudo fdisk -l /dev/sda - list the partition table information.

##### Partitions types

+ Primary Partition - used to boot the operating system (not more than 4 paritition in a disk)
+ Extended Partition - can't use it's own and can host logical partition (not more than 4 logical paritition in a disk)
+ Logical Partition

+ A disk is partioned is defined by partition scheme or partition table.
	* MBR(Master Boot Record) partition scheme is a type of partition scheme with 4 primary partitions and 
	maximum size of the a disc is 2TB and 4th partition is called as extended partition. 
	* GPT (G-U-I-D partition table)is type of partition scheme with unlimited no.of paritition per disc.
+ gdisk /dev/<partition disk> - to do partition. select "n" to add partition, type partition size
  and type "w" at the end to create new partition.
+ sudo fdisk -l /dev/<partition disk> - to check the created new partition.

### File System

+ File System How data is stored in disk.

#### Types of File System

<h5 align="center"> EXT2 </h5>

* Maximum Size is 2TB
* Maximum volume size is 4TB.
* Supports Compression
* Support Linux Permission
* long Crash recovery

<h5 align="center"> EXT3 </h5>

* Maximum Size is 2TB
* Maximum volume size is 4TB.
* Uses Journal
* Backwards Compatible

<h5 align="center"> EXT3 </h5>

* Maximum Size is 16TB
* Maximum volume size is 1Exabyte.
* Uses Journal
* Uses chksum for journal
* Backwards Compatible

#### working with EXT4

* mkfs.ext4 /dev/<partition disk> - to create EXT4 file system.
* mkdir /mnt/ext4
* mount /dev/<partition disk>  /mnt/ext4 - mounting the File System 
* mount | grep /dev/<partition disk> - to check whether filesystem mounted or not
* df -hP | grep dev/<partition disk> - to check whether filesystem mounted or not
* /etc/fstab - add an entry to file after restarting after mounting as follows in the table.

| Field| Purpose|
|------| -------|
|File System | such as /dev/<partition disk> to be mounted |
|Mountpoint | Directory to be mounted on |
| Type | Example ext2, ext3,ext4 |
| Options | such as RW-Read Write, RO- Read only|
| Dump | 0 - Ignore, 1-take backup |
| Pass | 0 - Ignote, 1or2 - FSCK (file system check enforced) |

Eg: **echo "/dev/sdb1 /mnt/ext4 ext4 rw 0 0" >> etc/fstab**

#### External Storage 

+ DAS - Direct attached storage
	* Block Storage
	* Fast and Reliable
	* Affordable
	* Dedicated to single host
	* Ideal for small Business
	
+ NAS - Network attached storage
	* NFS/CIFS
	* Reasonably Fast and Reliable
	* File Based Storage
	* Shared Storage
	* Not Suitable for OS install
	
+ SAN - Storage Area Network
	* FC or iSCSI
	* Block Storage
	* Fast, Secure and Reliable
	* High Availability
	* Expensive
	
### Logical Volume Manager

* apt-get install lvm2 - to install LVM
* pvcreate /dev/<paritition disk> - create physical volume object using free space
* vgcreate <volume name> /dev/<paritition disk> - create volume group
* pvdisplay - to see the physical value
* vgdisplay - to see all volume group
* lvcreate -L  <size> -n vol1 <volume name> - create logical volume
* lvdisplay - to see logical volume
* lvresise - to increase the logical volume





































Lab - Creating a new Partition

sudo gdisk /dev/vdd
[sudo] password for bob: 
GPT fdisk (gdisk) version 1.0.3

Partition table scan:
  MBR: not present
  BSD: not present
  APM: not present
  GPT: not present

Creating new GPT entries.

Command (? for help): n 
Partition number (1-128, default 1): 1
First sector (34-41943006, default = 2048) or {+-}size{KMGTP}: 2048
Last sector (2048-41943006, default = 41943006) or {+-}size{KMGTP}: +10G
Current type is 'Linux filesystem'
Hex code or GUID (L to show codes, Enter = 8300): 8300
Changed type of partition to 'Linux filesystem'

Command (? for help): w

Final checks complete. About to write GPT data. THIS WILL OVERWRITE EXISTING
PARTITIONS!!

Do you want to proceed? (Y/N): y
OK; writing new GUID partition table (GPT) to /dev/vdd.
The operation has completed successfully.
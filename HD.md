## Mount on Startup

Supose disk in /media/data

Get the unique ID for device:
> sudo blkid

Update fstab
> sudo nano /etc/fstab

Add this line at the bottom:
> UUID=14D82C19D82BF81E /media/data auto nosuid,nodev,nofail,x-gvfs-show 0 0

Explanation:

* /media/data is the location of the media
* auto means auto mount partition at boot
* nosuid specifies that the filesystem cannot contain set userid files. This prevents root escalation and other security issues.
* nodev specifies that the filesystem cannot contain special devices (to prevent access to random device hardware).
* nofail removes errorcheck
* x-gvfs-show show the mount option in the file manager. If this is on a GUI-less server, this option won't be necessary
* 0 determines which filesystems need to be dumped
* 0 determine the order in which filesystem checks are done at boot time (0 is the default)

## Format a partition inside a disk

Do not use mkfs, use specific command:

#### NTFS (example)
> mkntfs -f /dev/sdb1
f to do quick format

## List Drives

> lsblk
List partition type
> lsblk -f
List disk only
> lsblk | grep disk

## Operate on Disk

Select disk (example)
> sudo fdisk /dev/sdb

Inside fdisk:
* d delete partition
* w to flush changes

Delete all partitions
Create GPT table
Create partition


## Check health

> smartctl -a /dev/sdb
Look for 'SMART Error Log Version: 1'
It should say No errors logged

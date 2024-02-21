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

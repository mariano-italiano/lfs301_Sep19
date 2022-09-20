df -h
df -hT
ls -lai
ln -s plik1 softlink
ls -lai 
vi plik1
vi softlink 
rm plik1
ls -la
ls -lai
vi softlink 
ls -lai
cat plik1
cat softlink 
ln plik1 hardlink
ls -lia
cat plik1
cat hardlink 
vi plik1
cat plik
cat plik1
cat hardlink
vi hardlink 
cat plik1
rm plik1
vi hardlink 
cp hardlink hardlink2
ls -lai hardlink*
cd /usr/
ls -la
cd lib
ls -la
cd
ls -la
ls -lai
ln hardlink plik1
ls -lia
find . -inum 1048311
find . -inum 1050705
find . -samefile plik1
find / -samefile cat /proc/filesystems 
cat /proc/filesystems
df -hT 
clear
systemd-analyze 
systemd-analyze blame 
journalctl 
journalctl -b
journalctl sshd
which chornyd
which chronyd
journalctl /usr/sbin/chronyd
journalctl systemd
which systemd
which sshd
journalctl /usr/sbin/sshd
journalctl --help
journalctl -u chronyd
journalctl /usr/sbin/chronyd
journalctl --since=today
journalctl --since"-20min"
journalctl --since "-20min"
journalctl -p err
journalctl -f
journalctl -o verbose -u chronyd
journalctl -p err -o verbose
journalctl --since=today _SYSTEMD_UNIT="sshd.service"
cd /run/log/
ls
cd journal/
ls
cd 7222932c08884c78930162b6efb54242/
ls
less system
less system.journal 
ls -la
pwd
cd ..
mkdir /var/log/journal
systemctl restart systemd-journal
systemctl restart systemd-journald
pwd
ls -la
cd /var/log
ls -la journal/
ls -la journal/7222932c08884c78930162b6efb54242/
vi /etc/systemd/journald.conf 
systemctl restart systemd-journald
df -h
man df
df -a
df -hT
blkid
lsblk
partprobe
partprobe --help
cd
history
history | awk '$1 > 1002' | cut -c 8- > day2_history.md
cd lfs301_Sep19/bash_history/
mv /root/day2_history.md .
git status
git add day2_history.md 
git commit -m "Add day2 history"
git push
cd
cat /proc/partitions 
echo "- - -" > /sys/class/scsi_host/host0/scan 
for host in /sys/class/scsi_host/*; do echo host$ ;done
for host in /sys/class/scsi_host/*; do echo $host ;done
clear
cat /proc/partitions 
fdisk /dev/sdb
cat /proc/partitions 
fdisk /dev/sdb
cat /proc/partitions 
fdisk -l
fdisk -l /dev/sdb
cat /proc/partitions 
gdisk /dev/sdc
df -h
gdisk
gdisk /dev/sdc
cat /proc/partitions 
blkid
lsblk
df -h
fdisk /dev/sdb
pvcreate /dev/sdb
wipefs --help
pvs
pvdisplay 
vgcreate 
vgcreate vg0 /dev/sdb
vgs
vgdisplay 
vgcreate --help
lvcreate 
lvcreate --help
lvcreate -L 2G -n lv1 vg0
lvs
vgs
pvs
lvremove lv1
lvremove /dev/vg0/lv1 
vgremove vg0 
pvremove /dev/sdb
wipefs -a /dev/sdb
pvcreate /dev/sdb
vgcreate vg0 /dev/sdb
lvcreate -L 2G -n lv1 vg0
blkid
mkfs.ext4 /dev/mapper/vg0-lv1 
mkdir /lvm1
mount /dev/mapper/vg0-lv1 /lvm1/
df -h
cd /lvm1
ls -la
touch plik1
cd 
vi /etc/fstab 
blkid
vi /etc/fstab 
umount /lvm1
df -h
mount -a
df -h
cd /lvm1/
ls -la
cat plik1 
chmod +x plik1 
./plik1 
vi /etc/fstab 
cd 
umount /lvm1 
cd /lvm1/
cd ..
mount -a
cd /lvm1/
ls
ls -la
vi plik1 
which touch
./plik1 
/usr/bin/touch plik2
cd 
/lvm1
cd /lvm1
umount /lvm1
pwd
cd
umount /lvm1
vi /etc/fstab 
mount -a
cd /lvm1/
./pl
ls -la
./plik1
d 
cd 
vi /etc/fstab 
cat /proc/mounts 
umount /lvm1 ; mount -a
cat /proc/mounts | tail -1
clear
df -h
dd if=/dev/urandom of=/lvm1/bigfile1 bs=1024 count=1
dd if=/dev/urandom of=/lvm1/bigfile1 bs=1024 count=1024
dd if=/dev/urandom of=/lvm1/bigfile1 bs=1024 count=102400
dd if=/dev/urandom of=/lvm1/bigfile1 bs=1024 count=1024000
dd if=/dev/urandom of=/lvm1/bigfile2 bs=512 count=1024000
df -h
dd if=/dev/urandom of=/lvm1/bigfile3 bs=312 count=1024000
df -h
vgs
lvs
lvextend -L +2G /dev/vg0/lv1 
lvextend -L +100%FREE /dev/vg0/lv1 
lvextend -l +100%FREE /dev/vg0/lv1 
vgs
lvs
df -h
resize2fs /dev/vg0/lv1
df -h
dd if=/dev/urandom of=/lvm1/bigfile4 bs=2048 count=1024000
df -h
lvs
vgs
pvs
cat /proc/partitions 
pvcreate /dev/sdd 
vgextend vg0 /dev/sdd
vgs
lvextend -L +500M /dev/vg0/lv1
vgs
lvs
resize2fs /dev/vg0/lv1
df -h
history 
history | awk '$1 > 1002' | cut -c 8- > lfs301_Sep19/bash_history/day2_history.md
pvdisplay /dev/sdd 
pvs
vgs
lvs
pvs
lsblk
gdisk /dev/sdc
wipefs -a /dev/sdc
pvcreate /dev/sdc 
vgcreate vg1
vgcreate vg1 /dev/sdc
lvcreate -L 1G -n lv2 vg1
lvs
mkfs.xfs /dev/mapper/vg1-lv2 
mkdir /xfs
blkid 
vi /etc/fstab 
mount -a
df -h
df -hT
cd /xfs
ls -la
vgs
lvs
lvextend -L +10M lv2
lvextend -L +10M /dev/vg1/lv2
resize2fs /dev/vg1/lv2
xfs_growfs /dev/vg1/lv2
df -h
ls -la
mv /home/student/Downloads/* .
dd if=/dev/urandom of=bigfile bs=1024 count=102400
ls -la
ls -lah
pwd
df -hT
cd
xfsdump --help
xfsdump -f /xfs.dump /xfs
ls -lah /xfs.dump 
umount /xfs
lvs
lvreduce -L 200M /dev/vg1/lv2 
lvs
mkfs.xfs /dev/vg1/lv2 
mkfs.xfs -f /dev/vg1/lv2 
mount /dev/vg1/lv2 /xfs
xfsrestore -f /xfs.dump /xfs
cd /xfs
ls -la
cd
blkid
e2label /dev/mapper/vg0-lv1
e2label /dev/mapper/vg0-lv1 MbrPartition
e2label /dev/mapper/vg0-lv1
vi /etc/fstab 
xfs_admin /dev/mapper/vg1-lv2
xfs_admin -L XfsPartition /dev/mapper/vg1-lv2
umount /xfs
xfs_admin -L XfsPartition /dev/mapper/vg1-lv2
mount -a
blkid
vi /etc/fstab 
mount -a
cd /xfs
ls -la
cd
mount -o remount,ro /xfs
cat /proc/mounts | grep -i /xfs
mount -o remount,rw /xfs
cat /proc/mounts | grep -i /xfs
tune2fs -l /dev/sda1
e4defrag --help
e4defrag -c /var/log/
e4defrag -c /tmp
e4defrag -c /tmp/
e4defrag -c /var/
e4defrag -c /var/log/
e4defrag  /var/log/
e4defrag -c /var/log/
lastlog 
ip a 
ping almaLinux
mount almaLinux:/nfs-share /mnt
df -h
df -hT
cd /mnt
ls -la
touch plik4
ls -la
vi /etc/fstab 
cd ;umount /mnt
df -h
mount -a
vi /etc/fstab 
mount -a
df -h
mount --help
lsblk
gdisk /dev/sdc
pvs
vgs
lvcreate -L 1G -n lv_swap vg1
lvs
mkswap /dev/mapper/vg1-lv_swap 
blkid
vi /etc/fstab 
swapon -s
swapon -a
swapon -s
swapoff /dev/sda2
swapon -s
swapon -a
swapon -s
dd if=/dev/urandom of=swapfile bs=1024 count=1024
dd if=/dev/urandom of=swapfile bs=1024 count=10240
mkswap swapfile 
swapon swapfile
swapon -s
swapoff /dev/dm-2
swapoff /dev/sda2 
swapoff /root/swapfile 
swapon -s
vi /etc/fstab 
swapon -a
swapon -s
umount /xfs
umount /lvm1
vi /etc/fstab 
lvremove /dev/vg1/lv_swap 
swapoff /root/swapfile 
lvremove /dev/vg1/lv_swap 
swapon -s
swapoff /dev/dm-2
lvremove /dev/vg1/lv_swap 
lvremove /dev/vg0/lv1 
lvs
lvremove /dev/vg1/lv2 
lvs
vgs
vgremove vg[0,1]
vgremove vg0
vgremove vg1
vgs
pvs
vgcreate -v vg_stripe /dev/sd[b-d]
lvcreate -L 2G -i 3 -I 128k -n lv_stripe vg_stripe
lvdisplay -m /dev/vg_stripe/lv_stripe 
lvremove /dev/vg_stripe/lv_stripe 
vgremove vg_stripe 
vgs
pvs
fdisk /dev/sdb
cat /proc/partitions 
lsmod 
lsmod | grep -i dm
lsmod | grep -i dm_crypt
modprobe dm_crypt
lsmod | grep -i dm_crypt
dnf install cryptsetup
cat /proc/partitions 
cryptsetup -y luksFormat /dev/sdb1
cryptsetup luksOpen /dev/sdb1 secret
mkfs.ext4 /dev/mapper/secret 
mkdir /secretData
mount /dev/mapper/secret /secretData/
cd /secretData/
ls -la
echo "SecretPass" | base64 
echo "SecretPass" | base64 | base64
echo "SecretPass" | base64 | base64 | base64
cd
umount /secretData 
cryptsetup luksClose secret
cat /dev/mapper/
ls -la /dev/mapper/
ls -la /dev/mapper/control 
cd /dev/
ls
cd mapper/
ls
cd
lvs
vgs
pvs
fdisk /dev/sdb
fdisk
fdisk /dev/sdb
fdisk /dev/sdc
fdisk /dev/sdb
fdisk /dev/sdd
cat /proc/partio
cat /proc/partitions 
mdadm -E /dev/sd[b-d]1
mdadm --create /dev/md5 --level=5 --raid-devices=3 /dev/sd[b-d]1
mdadm --help
man mdadm
mdadm -D /dev/md5
lsblk
fdisk /dev/sdb
mdadm --manage --add /dev/md5 /dev/sdb2
mdadm -D /dev/md5
mkfs.xfs /dev/md5
mkdir /md5
mdadm --manage --fail /dev/sdc1
mkdir /md5
mdadm -D /dev/md5
mdadm --manage --fail /dev/md5 /dev/sdc1
mdadm -D /dev/md5
mdadm --detail --scan --verbose >> /etc/mdadm.conf
vi /etc/mdadm.conf
history
history | awk '$1 > 1002' | cut -c 8- >> lfs301_Sep19/bash_history/day2_history.md

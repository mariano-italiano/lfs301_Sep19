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

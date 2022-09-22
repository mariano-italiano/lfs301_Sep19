cat /proc/partitions
pvs /dev/sde
pvcreate /dev/sde
vgcreate vg_kvm /dev/sde
lvcreate -l 100%FREE -n lv_kvm vg_kvm
lvs
mkfs.xfs /dev/mapper/vg_kvm-lv_kvm
mkdir /kvm
mount /dev/mapper/vg_kvm-lv_kvm /kvm
mount -a
df -h
mkdir -pv /kvm/{disk,iso}
cp /usr/libexec/qemu-kvm /usr/libexec/qemu-system-x86_64
cp /usr/libexec/qemu-kvm /usr/libexec/qemu-system-x86_64 -rp
wget https://cdimage.debian.org/debian-cd/current/amd64/iso-cd/debian-11.5.0-amd64-netinst.iso
qemu-img --help
qemu-img create -f qcow2 /kvm/disk/debian.qcow2 15G
/usr/libexec/qemu-system-x86_64 -enable-kvm -name firstKvmVm
/usr/libexec/qemu-system-x86_64 -enable-kvm -name firstKvmVm -m 1G -drive format=raw,file=/kvm/disk/firstVm.qcow2 -net nic,model=virtio -display vnc=0.0.0.0:1
/usr/libexec/qemu-system-x86_64 -enable-kvm -name firstKvmVm -m 1G -drive format=raw,file=/kvm/disk/debian.qcow2 -net nic,model=virtio -display vnc=0.0.0.0:1
cd /var/lib/libvirt/
ls -la
vi /etc/libvirt/libvirt.conf
virt-install --virt-type=kvm --name debian1 --ram 1024 vcpus=2 \
cd
ls -la debian-11.5.0-amd64-netinst.iso
mv debian-11.5.0-amd64-netinst.iso /var/lib/libvirt/images/
virt-install --virt-type=kvm --name debian1 --ram 1024 vcpus=2 --cdrom=/var/lib/libvirt/images/debian-11.5.0-amd64-netinst.iso --network=bridge=virbr0,model=virtio --graphics vnc --disk path=/kvm/disk/debian.qcow2
virt-install --virt-type=kvm --name debian1 --ram 1024 --vcpus=2 --cdrom=/var/lib/libvirt/images/debian-11.5.0-amd64-netinst.iso --network=bridge=virbr0,model=virtio --graphics vnc --disk path=/kvm/disk/debian.qcow2
virsh edit debian1
virsh list
virsh list --all
virt-builder --list
virt-builder ubuntu-20.04 --size=10G --format qcow2 -o /kvm/disk/ubuntu20.qcow2 --hostname ubuntu20 --network --timezone Europe/Warsaw
virt-builder ubuntu-20.04 -o /kvm/disk/ubuntu20.qcow2 --hostname ubuntu20 --network --timezone Europe/Warsaw
virsh list
virsh list --all
virt-install --import --name ubuntu20 --ram 2048 --vcpu 2 --disk path=format=qcow2 --network=bridge=virbr0,model=virtio --noautoconsole
virt-install --import --name ubuntu20 --ram 2048 --vcpu 2 --disk path=/kvm/disk/ubuntu20.qcow2,format=qcow2 --network=bridge=virbr0,model=virtio --noautoconsole
virsh list --all
virsh console ubuntu20
virsh destroy ubuntu20
virsh list --all
virsh undefine ubuntu20


yum install snapd
ln -s /var/lib/snapd/snap /snapd
ln -s /var/lib/snapd/snap /snap
ls -la /var/lib/snapd/snap
ls -la /snap
systemctl enable --now snapd.socket
systemctl status snapd.socket
systemctl enable --now snapd.service
systemctl status snapd.service
q
snap install lxd
cat /proc/partitions
echo "- - -" > /sys/class/scsi_host/host0
echo "- - -" > /sys/class/scsi_host/host0/scan
echo "- - -" > /sys/class/scsi_host/host1/scan
cat /proc/partitions
lxd init
reboot
lxd init
lxc image list images:
lxc image list images: | grep -i almalinux
lxc launch 98c46b5be5fc alma9
lxc launch images:98c46b5be5fc alma9
lxc list
lxc image list images: | grep -i ubuntu
lxc image list images: | head
lxc launch images:d37b75f51a4f ubuntu
lxc list
lxc stop alma9
lxc list
lxc start alma9
ping 10.190.149.71
lxc exec ubuntu bash
ssh 10.190.149.71
lxc list
lxc launch images:d37b75f51a4f ubuntu2
lxc launch images:d37b75f51a4f ubuntu3
lxc launch images:d37b75f51a4f ubuntu4
lxc list
lxc exec alma9
lxc exec alma9 bash
lxc list
lxc exec alma9 bash
lxc list
lxc launch images:98c46b5be5fc alma9-2
lxc exec alma9-2 bash
lxc list
lxc exec alma9-2 bash
lxc list
ssh fd42:70de:30c1:2404:216:3eff:fed9:a46f
lxc exec alma9 bash
lxc delete -f alma9-2
lxc list
lxc profile list
lxc profile copy default web
lxc profile edit web
lxc config set alma9 boot.autostart true
lxc config get alma9 boot.autostart
lxc config get ubuntu boot.autostart
lxc config get ubuntu
vi skrypt.sh
chmod +x skrypt.sh
lxc file push skrypt.sh ubuntu/tmp/
lxc file push skrypt.sh ubuntu2/tmp/
lxc file push skrypt.sh ubuntu3/tmp/
lxc file push skrypt.sh ubuntu4/tmp/
lxc exec ubuntu4 bash
lxc exec ubuntu3 bash /tmp/skrypt.sh
lxc exec ubuntu2 bash /tmp/skrypt.sh > /tmp/install.log
lxc file pull ubuntu2/tmp/install.log .
lxc exec ubuntu2 bash
lxc exec ubuntu1 "bash /tmp/skrypt.sh > /tmp/install.log"
vi skrypt.sh
lxc file push skrypt.sh ubuntu2/tmp/
lxc exec ubuntu2 bash /tmp/skrypt.sh
lxc file pull ubuntu2/tmp/install.log .
ls -la install.log
less install.log
lxc snapshot ubuntu
lxc snapshot ubuntu --help
lxc snapshot ubuntu snap1
lxc snapshot list
lxc snapshot ubuntu list
lxc snapshot ubuntu snap1
lxc list
lxc info ubuntu
lxc config device set ubuntu3 eth0 ipv4.address 10.190.149.113
iptables -L -v
curl -fsSL https://get.docker.com/ | sh
dnf remove doscker
yum remove docker
curl -fsSL https://get.docker.com/ | sh
yum install -y -q docker-ce docker-ce-cli containerd.io docker-scan-plugin docker-compose-plugin docker-ce-rootless-extras
yum remove docker-common
curl -fsSL https://get.docker.com/ | sh
systemctl status docker
systemctl enable --now docker
systemctl status docker
docker search nginx
docker pull nginx
docker search mariadb
docker inspect mariadb
docker inspect nginx
docker run --help
docker run -d -it nginx web1
docker ps
docker ps -a
docker logs strange_taussig
docker run -d -it nginx --name web1
docker ps
docker ps -a
docker run -d -it nginx
docker ps -a
docker ps
docker run -d -it --name web1 nginx
docker ps
docker logs web1
docker ps
docker ps -a
docker rm pedantic_wilbur
docker rm pedantic_wilbur -f
docker rm elastic_roentgen
docker rm strange_taussig
docker ps
docker ps -a
docker run -d -it --name web2 -m 512m --memory-reservation=256m -v /tmp:/tmp -p 8080:80 nginx
docker ps -a
docker info web2
docker info
docker inspect web2
docker inspect web2 | grep memory -i
docker ps
docker exec web2 bash
docker exec -it web2 bash
ls -la /tmp
cp -rp /usr/lib/systemd/system/sshd.service /etc/systemd/system/docker-web2.service
vi /etc/systemd/system/docker-web2.service
which docker
vi /etc/systemd/system/docker-web2.service
docker start --help
vi /etc/systemd/system/docker-web2.service
systemctl daemon-reload
docker ps
docker stop web1
docker stop web2
docker ps
docker ps -a
systemctl start docker-web2.service
docker ps -a
systemctl stop docker-web2.service
docker ps -a

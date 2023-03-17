# Partitioning, Formatting, and Mounting a Hard Drive in Linux Ubuntu Server

sudo fdisk -l diskinizi görün

sudo parted /dev/sdb  Benim eklediğim ikinci disk

sudo mkfs.ext4 /dev/sdb   format at

sudo mkdir /mnt/name  Mnt altında dizin oluştur

sudo mount /dev/sdb /mnt/name  sonra dizine bağla

nano /etc/fstab  içine aşağıdaki satırı en alta ekle

/dev/sdb /mnt/name ext4 defaults 0 0

mount | grep sdb bu komutla mount durumunu gör

Unmounting etmek istersen 

sudo umount /dev/sdb

sudo umount -l /dev/sdb

sudo -s
cd /etc/apt/apt.conf.d
curl http://www.beegfs.com/release/latest-stable/dists/beegfs-deb8.list > beegfs-deb8.list
apt-get update
curl http://www.beegfs.com/release/beegfs_2015.03/gpg/DEB-GPG-KEY-beegfs | apt-key add -

atp-get install -yq beegfs-mgmtd beegfs-meta beegfs-storage

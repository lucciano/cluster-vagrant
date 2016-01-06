https://moosefs.com/Content/Downloads/moosefs-installation.pdf

On every master node:

~~~~~~~~~~~~~~~~~~~~~~~~~~{.console}
sudo apt-get update
sudo apt-get install moosefs-master
sudo cp /etc/mfs/mfsmaster.cfg.dist /etc/mfs/mfsmaster.cfg
sudo vi /etc/default/moosefs-master
sudo cp /etc/mfs/mfsexports.cfg.dist /etc/mfsexports.cfg
sudo /etc/init.d/moosefs-master start
~~~~~~~~~~~~~~~~~~~~~~~~~~

On every monitor node:

~~~~~~~~~~~~~~~~~~~~~~~~~~{.console}
sudo apt-get install moosefs-cgiserv
sudo apt-get install moosefs-cgiserv moosefs-cgi
sudo vi /etc/default/moosefs-cgiserv
sudo service moosefs-cgiserv start
~~~~~~~~~~~~~~~~~~~~~~~~~~


On every chunk node:

~~~~~~~~~~~~~~~~~~~~~~~~~~{.console}
sudo apt-get install moosefs-chunkserver
sudo vi /etc/default/moosefs-chunkserver
sudo mkdir /mnt/mfschunks1
sudo mkdir /mnt/mfschunks2
sudo chown mfs:mfs -R /mnt/mfschunks1 /mnt/mfschunks2 
sudo cp /etc/mfs/mfschunkserver.cfg.dist /etc/mfs/mfschunkserver.cfg
sudo cp /etc/mfs/mfshdd.cfg.dist /etc/mfs/mfshdd.cfg
sudo vi /etc/mfs/mfschunkserver.cfg
sudo vi /etc/mfs/mfshdd.cfg
sudo service moosefs-chunkserver start
~~~~~~~~~~~~~~~~~~~~~~~~~~

On every client:
~~~~~~~~~~~~~~~~~~~~~~~~~~{.console}
sudo apt-get install moosefs-client fuse
sudo mkdir -p /mnt/mfs
sudo mfsmount /mnt/mfs -H mfsmaster
~~~~~~~~~~~~~~~~~~~~~~~~~~


TODO: Encription, add/remove nodes/capacity, test releas 3.0

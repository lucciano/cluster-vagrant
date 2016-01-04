ssh-keygen

echo 192.168.15.11 node01 >> /etc/hosts
echo 192.168.15.12 node02 >> /etc/hosts
echo 192.168.15.13 node03 >> /etc/hosts
echo 192.168.15.14 node04 >> /etc/hosts
~                    
ssh-copy-id vagrant@node01
ssh-copy-id vagrant@node02
ssh-copy-id vagrant@node03
ssh-copy-id vagrant@node04

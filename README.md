# create_virtual_host

To change localhostname
  [root@localhost ~]# [root@localhost ~]#
   hostnamectl set-hostname linuxshelltips.in
   
   Fix Error: add port to the firewall:

Red Hat Enterprise Linux and CentOS

command to list currently open ports.

firewall-cmd --list-ports

command to list zones.

firewall-cmd --get-zones

command to list the zone containing eth0.

firewall-cmd --get-zone-of-interface=eth0

command to open port 81 for TCP traffic.

firewall-cmd --add-port 81/tcp

firewall-cmd --reload

command to open port 81 for TCP traffic after reboot. Use this command to make changes persistent.

firewall-cmd --permanent --add-port 81/tcp

command to open a range a range of ports.

firewall-cmd --permanent --add-port 60000-61000/tcp

command to stop and start the firewall.

systemctl stop firewalld 

systemctl start firewalld

firewall-cmd --zone=public --permanent --add-service=http

In case you wish to close a specific port use the --remove-port option.

Fixing when Permission denied: make_sock: could not bind to address [::]:91
dnf provides */semanage
sudo dnf install policycoreutils-python-utils
Example: allow port 91 for httpd domain processes
sudo semanage port -a -t http_port_t -p tcp 91

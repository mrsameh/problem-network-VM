# Problem-network-VM
Fix bug network VM Linux in VMware and VirtualBox

1- Access in /etc/init.d
cd /etc/init.d
2- Create file withe name : net-autostart
touch net-autostart
3- Write this code in the file net-autostart

#!/bin/bash
# Solution for acces network with VM
#
#
### BEGIN INIT INFO
# Default-Start: 2 3 4 5
# Default-Stop: 0 1 6 
### END INIT INFO
dhclient -v

# Take this file with autorisation and execute
chmod 755 net-autostart
# Add the script in the auto start with system
chkconfig --add net-autostart

4- save and reboot the machine

 

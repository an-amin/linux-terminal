List of Steps to Change the CentOS SSH Port Number
The following are the steps to be performed to change default SSH port number on CentOS:

1. Login to the CentOS server.
2. Back up then edit the /etc/ssh/sshd_config file.
3. Add the line Port XXXX to the file, where XXXX is the new port number.
4. Update the SELinux policy for the new SSH port.
5. Update the iptables (CentOS 6) or firewalld (CentOS 7) firewall rule for the new SSH port.
6. Restart the services or the server.
7. Check the changes worked by connecting on the new port.

To start the process to change the SSH port number, log into the server. Before editing the /etc/ssh/sshd_config file take a copy in case anything goes wrong. Here's the command to copy sshd_config to sshd_cfg_old:

``
sudo cp /etc/ssh/sshd_config /etc/ssh/sshd_cfg_old
``

(For all commands in this article only enter the text after the # or $ prompt character, as seen on the terminal screen.)

Editing is done with vi or nano. On a minimal CentOS install, typical for a VPS, nano will not be installed by default. To edit sshd_config using vi:

``
sudo vi /etc/ssh/sshd_config
``

Update SELinux with the New Port Number
If the Security Enhanced Linux module (SELinux) is running then update selinux with the new port number. Failure to update SELinux for the new port will result in a Permission denied showing in the SELinux log. To check that selinux is enabled run sestatus. (In these examples the command is on the first line, and if shown, the result of the command is displayed from the second line onwards, which may differ depending upon your system.):

````
# sestatus
SELinux status:             enabled 
SELinuxfs mount:            /sys/fs/selinux
SELinux root directory:     /etc/selinux
Loaded policy name:         targeted
Current mode:               enforcing
Mode from config file:      enforcing
Policy MLS status:          enabled
Policy deny_unknown status: allowed
Policy version:             28
````



Use semanage to add the new port number to SELinux, see the article RHEL 6: semanage SELinux Command Not Found on how to install the command if not present (e.g. if using the CentOS minimal install). For this article this command was used to check the package for semanage:


``
sudo yum provides /usr/sbin/semange
``

Or:

``
sudo yum whatprovides /usr/sbin/semanage
``


And this command to install it (remove the -y to manually confirm the install):

``
sudo yum -y install policycoreutils-python
``

The port numbers for SELinux can be displayed using a semanage command (pipe to less to page through the list):

``
semanage port -l | less


In the list of ports will be found ssh_port_t tcp 22. Use semanage to add the new port number:

``
sudo semanage port -a -t ssh_port_t -p tcp 2132``
``



Restart sshd 
``
sudo systemctl restart sshd.service
``

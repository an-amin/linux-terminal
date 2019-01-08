``
yum provides /usr/sbin/semange
``
Or:
``
yum whatprovides /usr/sbin/semanage
``
``
yum -y install policycoreutils-python
 ``

Open shhd configuration file with super user permission:
``
sudo nano /etc/ssh/sshd_config
``

Change `# Port 22` to `Port 2121` or {port number} you like...

``
semanage port -a -t ssh_port_t -p tcp 2121
``

Restart sshd 
``
sudo systemctl restart sshd.service
``

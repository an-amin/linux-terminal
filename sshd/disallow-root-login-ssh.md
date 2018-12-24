``
nano /etc/ssh/sshd_config
``

Change: 
``
# PermitRootLogin Yes
``

To: 
``
PermitRootLogin no
``

``
sudo systemctl restart sshd
``

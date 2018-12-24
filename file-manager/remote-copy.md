Copy a file from local host to remote host
``
scp local/path/to/file.txt user@host:/remote/path/dir/
``

Copy a file from remote host to lcoal host
``
scp user@host:/remote/path/to/file.txt local/path/to/dir/
``

if ssh default port is changed
``
scp -p {port_number} ... ...
``

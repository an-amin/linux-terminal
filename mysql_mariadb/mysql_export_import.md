### Export a database:
mysqldump -h {host} -u {user} -p -P {port_no} {db_name} > {exported_file_name}

````
mysqldump -h localhost -u root -p -P 3306 test_db > /path/to/db_file.sql
````

### Export schema without data 
mysqldump -h {host} -u {user} -p -P {port_no} --no-data {db_name} > {exported_file_name}

````
mysqldump -h localhost -u root -p -P 3306 --no-data test_db > /path/to/db_file.sql
````


### File name with timestamp
````
mysqldump -h localhost -u root -p -P 3306 test_db > /path/to/"DB_FileName `date +"%F %T"`.sql"
````


### Import a database: 
mysql -h {host} -u {user} -p -P {db_name} < {db_file} 

````
mysql -h localhost -u root -p -P 3306 db_name < /path/to/db_file.sql
````


##### -P {port} is optional if default port is not changed***

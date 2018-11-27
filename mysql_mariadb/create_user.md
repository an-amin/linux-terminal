
## creating a user
### CREATE USER '{user}'@'{host}' IDENTIFIED BY '{password}';
`CREATE USER 'admin'@'%' IDENTIFIED BY '12345678';`
`CREATE USER 'user'@'%' IDENTIFIED BY '12345678';`


## all privileges
### GRANT ALL PRIVILEGES ON * . * TO '{user}'@'{host}';
`GRANT ALL PRIVILEGES ON * . * TO 'admin'@'%';`


## or privilege based on wildcard  matching
### grant all on '{name}\_%'.* to '{user}'@'{host}';
`grant all on '{name}\_%'.* to '{user}`@'{host}';`



## apply changes
`FLUSH PRIVILEGES;`

## Exit mysql
`quit;`
### or, 
`exit;`


### reference 
{user} 		= database username
{password} 	= password 
{host} 		= databse serve hostname. 'localhost' or '%' (anyhost)
{name} 		= database name

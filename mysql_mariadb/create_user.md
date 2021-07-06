
## creating a user
### CREATE USER `{user}`@`{host}` IDENTIFIED BY '{password}';
````CREATE USER `admin`@`%` IDENTIFIED BY '12345678';````

````CREATE USER `user`@`%` IDENTIFIED BY '12345678';````


## all privileges
### GRANT ALL PRIVILEGES ON * . * TO `{user}`@`{host}`;
````GRANT ALL PRIVILEGES ON * . * TO `admin`@`%`;````


## or privilege based on wildcard  matching
### grant all on '{name}\_%'.* to `{user}`@`{host}`;
```grant all on `user\_%`.* to `user`@`%`;```


## GRANT root privilege
### GRANT ALL PRIVILEGES ON * . * TO `{user}`@`{host}` WITH GRANT OPTION;
````GRANT ALL PRIVILEGES ON * . * TO `admin`@`%` with grant option;````


## apply changes
`FLUSH PRIVILEGES;`

## Exit mysql
`quit;`
### or, 
`exit;`


### reference 
{user} 		= database username
{password} 	= password 
{host} 		= databse serve hostname. `localhost` or `%` (anyhost)
{name} 		= database name


### Create backup user agent
````
create user `backup_agent`@`localhost` IDENTIFIED BY 'backup_agent_user_password';
grant all on `backup\_%`.* to `backup_agent`@`localhost`;
grant SHOW DATABASES, SELECT, LOCK TABLES, RELOAD, SUPER on *.* to `backup_agent`@`localhost`;
FLUSH PRIVILEGES;
````

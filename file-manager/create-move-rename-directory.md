Create a directory in current location

````
mkdir directory_name
````

to know current location
````
pwd
````
it will return current lcoation like: `/current/path`

to Create a directory in other location

````
mkdir /path/to/directory_name
````

if `/path/to/` is not exists and we want to create those directory as well
```
mkdir -p /path/to/directory_name
```
now the directory `/path/` & `to/` will also be created while creating `directory_name`


rename directory
```
mv /path/to/directory /path/to/new_directory_name
```

move  directory
```
mv /path/to/directory /new/path/to/directory_name
```


move & rename directory
```
mv /path/to/directory /new/path/to/new_directory_name
```

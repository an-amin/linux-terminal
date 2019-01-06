````
touch filename.extension
````

````
touch file.txt
````

File name with Timestamp
````
touch /path/to/file/"name_$(date +%F_%R).txt"
````
it will create a file named `name_2018-02-28_13:25.txt`


````
touch /path/to/file/"name_$(date +%Y/%m/%d_%H-%i-%s).txt"
````
it will create a file named `name_2018/02/28_13-25-05.txt`


to rename file
```
mv /path/to/fileName.txt /path/to/newFileName.txt
```

to move a file from one location to another
````
mv /path/of/the/file.txt /new/path/
````

move and rename
````
mv /path/of/the/file.txt /new/path/newFileName.txt
````

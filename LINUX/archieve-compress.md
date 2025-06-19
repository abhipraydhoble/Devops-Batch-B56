 ## $${\color {red} \textbf {Archeiving: compile all flders and files in one file}}$$
 ## Compression: reduce size of file

 - c create new archieve
 - v verbose
 - f filename
 - z gzip (reduce file size)
 - x extact  
 - C  extract at diff location

**example:**
````
du -sh /etc
````
####  check size of file/dir

**to create backup:**

````
tar -cvzf backup.tar.gz /etc
````

**to extract:**
````
tar -xvzf backup.tar.gz -C /opt
````

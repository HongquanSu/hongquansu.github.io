---                                                                                                                                                                                                                                                       
layout: default
title: "Useful tools for Astronomy"
tagline: 
---

## Bash

### Basic

For loop :
```
for i in *; do echo $i; done
```

Check if a file exist or not (more [file test operators](https://www.tldp.org/LDP/abs/html/fto.html)):
```
if [ -e ${file_name} ]; then echo ${file_name}; fi
```

Find out the number of files in a folder:
```
ls | wc -l
Note 1 : a folder is one file no matter how much files in it
Note 2 : ls -l | wc -l will give (the number of files + 1)
```

Generate a random number between 0 and N (not include), where N is an integer :
```
echo $(( RANDOM % N )) 
```

### Unzip or untar

Untar a .tar file :
```
tar -xvf filename.tar
Note: .tar is the extension for the source files downloaded from the arXiv.org 
```

### Errors

syntax error: unexpected end of file
```
might be caused by incomplete loops, e.g. if 'done' is missed in the following :
while :
do
    echo 'check me'
done
```

---                                                                                                                                                                                                                                                       
layout: default
title: "Useful tools for Astronomy"
tagline: 
---

## Bash

### Basic
Save the output of a command to a variable :
```
a=$(echo xyz); echo $a

>>> xyz
```

Write the output to a file :
- overwrite the file
```
echo 'writing test' > file_name.txt
```
- append to the file
```
echo 'writing test' >> file_name.txt
```

Get the last several characters of a string :
```
a=my.fits; echo "${a: -5}"
```
- Output is
```
.fits
```

Get the characters of a string before several charactors :
```
a=my.fits; echo "${a: :-5}".sdf
```
- Output is
```
my.sdf
```
- works on Ubuntu not on Mac

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

Extract substring :
```
b=${a:2:3}
```
- 2 is the zero-based offset and 3 is the length



### Unpack (unzip, untar) files

Unpack a .tar file :
```
tar -xvf filename.tar
Note: .tar is the extension for the source files downloaded from the arXiv.org 
```

Unpack a .tar.gz file :
```
tar -zxvf file.tar.gz
```

Unpack a .gz file:
```
gunzip file.gz
```

### Errors

syntax error: unexpected end of file
- might be caused by incomplete loops, e.g. if 'done' is missed in the following :
```
while :
do
    echo 'check me'
done
```

# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
To practice Linux Commands and Shell Scripting

# DESIGN STEPS:

### Step 1:

Navigate to any Linux environment installed on the system or installed inside a virtual environment like virtual box/vmware or online linux JSLinux (https://bellard.org/jslinux/vm.html?url=alpine-x86.cfg&mem=192) or docker.

### Step 2:

Execute the following commands

### Step 3:

Testing the commands for the desired output. 

# COMMANDS:
### Create the following files file1, file2 as follows:
cat > file1
```
chanchal singhvi
c.k. shukla
s.n. dasgupta
sumit chakrobarty
^d
```
cat > file2
```
anil aggarwal
barun sengupta
c.k. shukla
lalit chowdury
s.n. dasgupta
^d
```
### Display the content of the files
cat < file1
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/e3ad88c9-fa3b-4121-a67f-b833a9aa25de)
cat < file2
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/31925f5f-1bbd-4be6-a79a-608ccf3ba235)
# Comparing Files
cmp file1 file2
## OUTPUT
 ![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/3389e68c-7726-476f-9f1b-e533f5e50f60)
comm file1 file2
 ## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/b2a156fd-ffdf-4131-bc33-3edd002602e3) 
diff file1 file2
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/abbeb276-39b6-4cab-9aa1-f4db06d279d1)
#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```


cut -c1-3 file11
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/951c1653-42f1-43dd-9b12-556ecebfa654)
cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/10f91521-6bfb-41da-a08d-1890324c68c3)



cut -d "|" -f 2 file22
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/16df1d30-efb7-4d42-a082-8a0496f3c5f8)


cat < newfile 
```
Hello world
hello world
^d
````
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/a4e3202e-cd4c-4a31-b30d-c6f80760a057)


grep hello newfile 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/6d325650-ff19-4881-96a7-6cd15eee945c)




grep -v hello newfile 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/188b7150-7502-45fc-b6a0-338d2b4d3b92)
cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/d63e9915-25d6-44f9-b891-187634f6cb30)

cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/08dbe5b3-6261-45b4-876e-19799d475671)
grep -R ubuntu /etc
## OUTPUT
grep -w -n world newfile   
## OUTPUT


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
 ```
egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/e9973dc8-6ab1-4b0a-aa74-f83276069f88)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/1adfbb34-301d-43db-b77f-6822a9a6f902)
egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/dfa59802-0a75-49f6-948d-5cd573ca4fab)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/b5c9e88b-5bed-435c-9a54-95caa9707d35)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/75374eee-8a7d-4e74-a803-471c52355d83)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/a126c0f3-d5e3-44db-8a57-7917ca290017)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/e2406261-7472-49d3-9fea-46e930077d02)



egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/0c53d1d5-250c-4395-80fc-d7373cd8245f)



egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/037e8a95-ce98-49a1-b605-7312074b0ad2)

egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/be67e3f9-e71e-40bc-a2fc-7c6c88870740)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/515faa18-477e-49c4-b90b-3db3f50ff6ec)



egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/e67008a0-abed-4465-9bb8-b029c090109c)


cat > file23
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
1003 | Joe |  7000 | Developer
1001 | Ram | 10000 | HR
^d
```


sed -n -e '3p' file23
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/5c744f86-e5c2-43ec-9f20-3c2c43b6c205)



sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/44447969-e243-43dc-a245-341dfe1f62a7)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/2d1988c4-30fb-4895-b401-bd9b6ed5b13b)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/bfb15527-10ad-4f06-ab68-4127870fc290)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/8ccb3dcd-9b75-4ab3-acde-adc08512e7f0)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/70d5dd86-23aa-4b1a-98a8-ba443f632138)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/1c5f0e3e-2890-4558-8cf9-3cc8f2348aaa)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/64f44fd6-393d-4772-98f3-0b84cbc368fb)



seq 10 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/e0015fd6-b4a7-4de9-a947-822cb6959a80)



seq 10 | sed -n '4,6p'
## OUTPUT

![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/e85e36d9-496b-4b1f-9527-38f78435ed87)


seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/f4a0b3d1-cbff-44d4-b707-b1b98ece871c)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/3261c38f-0776-4b9d-bc21-70b0f3b8684f)



seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/9a6b7b13-7bc0-46ad-95ad-cc04ce53a472)


seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/306540b3-4e55-43bd-8886-ebdcaa55f516)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/b5dd22ec-8428-44bb-9d16-8aaa9e857b24)


sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/98d253b7-7da2-4e3f-b6a3-ad9e60eede79)


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
sort file21
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/8ca6ccc3-e80b-4624-8248-f65a78a8eb4c)


cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
``` 
uniq file22
## OUTPUT

![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/ea1862fb-3a15-4663-a5e6-c3068737e8c9)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/151ebcec-70db-49da-99aa-e43d36c58ecb)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/1b821619-02fb-48f7-9f0c-e0ebff8e4a68) 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/2d9a2cac-a7b0-4ff2-87fb-b5509227c004)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/a82e51da-7e7e-4643-a2d3-e5e3e22030fb)
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/62c74cf3-b39e-4187-8d01-72d734716f98)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/d7e45e5d-536f-4272-b839-20a4e5c14f0a)


cat < scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $1#
echo 'The $$ is ' $$
ps
^d
 ```

cat scriptest.sh 
```bash
\#!/bin/sh
echo “File name is $0 ”
echo "File name is " `basename $0`
echo “First arg. is ” $1
echo “Second arg. is ” $2
echo “Third arg. is ” $3
echo “Fourth arg. is ” $4
echo 'The $@ is ' $@
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```
 
chmod 777 scriptest.sh
 
./scriptest.sh 1 2 3

## OUTPUT

 ![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/bc6cee26-f029-4030-bb14-35c4ddf9fd59)

ls file1
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/92c9c0cb-db41-4b29-a9ea-eec4a5a7b33f)

echo $?
## OUTPUT 
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/54338d08-f986-49b3-ad4a-45eeb5e0db4d)

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/f70deac8-de95-4f91-a97b-459765f200b7)


 
# mis-using string comparisons

cat < strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
^d
```

cat strcomp.sh 
```bash
\#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/a24c1c5b-5121-4cb6-9d95-3584d2cac1b2)

# check file ownership
cat < psswdperm.sh 
```bash
\#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
^d
```

cat psswdperm.sh 
```bash
/#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
# check if with file location
cat>ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```
cat ifnested.sh 
```
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```

./ifnested.sh 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/d499c500-ff55-422c-b55a-d663f3966d7b)



# using numeric test comparisons
cat > iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
^d
```


cat iftest.sh 
```bash
\#!/bin/bash
val1=10
val2=11
if [ $val1 -gt 5 ]
then
echo “The test value $val1 is greater than 5”
fi
if [ $val1 -eq $val2 ]
then
echo “The values are equal”
else
echo “The values are different”
fi
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/17c81b14-22e2-4ebf-aff6-ee16aa8dfa51)

# check if a file
cat > ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
^d
```

cat ifnested.sh 
```bash
\#!/bin/bash
if [ -e $HOME ]
then
echo “$HOME The object exists, is it a file?”
if [ -f $HOME ]
then
echo “Yes,$HOME it is a file!”
else
echo “No,$HOME it is not a file!”
if [ -f $HOME/.bash_history ]
then
echo “But $HOME/.bash_history is a file!”
fi
fi
else
echo “Sorry, the object does not exist”
fi
```
# looking for a possible value using elif
cat elifcheck.sh 
```bash
\#!/bin/bash
if [ $USER = Ram ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Rahim ]
then
echo "Welcome $USER"
echo "Please enjoy your visit"
elif [ $USER = Robert ]
then
echo "Special testing account"
elif [ $USER = gganesh ]
then
echo "$USER, Do not forget to logout when you're done"
else
echo "Sorry, you are not allowed here"
fi
```

$ chmod 755 elifcheck.sh
 
$ ./elifcheck.sh 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/d2038620-b24a-4fa6-9447-0fc50985a4b7)


# testing compound comparisons
cat> ifcompound.sh 
```bash
\#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
$ chmod 755 ifcompound.sh
$ ./ifcompound.sh 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/9e7df29c-4bb8-4f20-b57c-5dfe6c60bbcc)

# using the case command
cat >casecheck.sh 
```bash
case $USER in
Ram | Robert)
echo "Welcome, $USER"
echo "Please enjoy your visit";;
Rahim)
echo "Special testing account";;
gganesh)
echo "$USER, Do not forget to log off when you're done";;
*)
echo "Sorry, you are not allowed here";;
esac
```
$ chmod 755 casecheck.sh 
 
$ ./casecheck.sh 
 
cat > whiletest
```bash
#!/bin/bash
#while command test
var1=10
while [ $var1 -gt 0 ]
do
echo $var1
var1=$[ $var1 - 1 ]
done
```
$ chmod 755 whiletest.sh
 
$ ./whiletest.sh
 ## OUTPUT:
 ![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/52a6cc69-f45d-4185-a5aa-8985221469af)

 
cat untiltest.sh 
```bash
\#using the until command
var1=100
until [ $var1 -eq 0 ]
do
echo $var1
var1=$[ $var1 - 25 ]
done
``` 
$ chmod 755 untiltest.sh
 ## OUTPUT:
 ![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/ce1dd629-cfa0-4568-99f0-2afaf6880e6e)
cat forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 ## OUTPUT:
 ![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/b309a4c5-0de3-4346-803d-93b2beead543)

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 ## OUTPUT:
 ![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/d5d081d0-43bf-4c0a-aee8-033ab6631960)

cat forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
```
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
 
cat forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh

## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/1701f311-47fa-44f5-9a58-59d19e2a90cc)

cat forinfile.sh 
```bash
#!/bin/bash
# reading values from a file
file="cities"
for state in `cat $file`
do
echo "Visit beautiful $file“
done
```
$ chmod 777 forinfile.sh
$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
````
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/15893dc0-a73b-4890-9fba-fb6f28f6958a)

cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype1.sh
$ ./forctype1.sh 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/04e92232-6b8c-4916-92a8-9e7feb6a6274)

cat fornested1.sh 
```bash
#!/bin/bash
# nesting for loops
for (( a = 1; a <= 3; a++ ))
do
echo "Starting loop $a:"
for (( b = 1; b <= 3; b++ ))
do
echo " Inside loop: $b"
done
done
```
$ chmod 755 fornested1.sh
 
$ ./fornested1.sh 
 ## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/a4e04ae0-2da0-403f-9687-fdae47cef7f9)

 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
break
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/ae314cdd-8073-4dc4-a450-741c609cd87b)

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 
 
cat forbreak.sh 
```bash
#!/bin/bash
# breaking out of a for loop
for var1 in 1 2 3 4 5
do
if [ $var1 -eq 3 ]
then
continue
fi
echo "Iteration number: $var1"
done
echo "The for loop is completed“
```

 
$ chmod 755 forcontinue.sh
 
$ ./forcontinue.sh 
## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/9c865b9c-4c8a-4279-b03d-56a655b04658)
 
cat exread.sh 
```bash
#!/bin/bash
# testing the read command
echo -n "Enter your name: "
read name
echo "Hello $name, welcome to my program. "
 ```
 
$ chmod 755 exread.sh 
 
$ ./exread.sh 
## OUTPUT

![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/df52304e-cd27-483d-8b9e-aa6d0368bef0)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/588a7135-258d-4131-be71-4b474b68551a)



$ ./exread1.sh 
 
cat funcex.sh
```bash
#!/bin/bash
# trying to access script parameters inside a function
function func {
echo $[ $1 * $2 ]
}
if [ $# -eq 2 ]
then
value=`func $1 $2`
echo "The result is $value"
else
echo "Usage: badtest1 a b"
fi
```
## OUTPUT

 ./funcex.sh 

 ![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/6d1c0929-7f38-482e-85db-d1d934c7d7e0)

 ./funcex.sh 1 2
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/8ea64856-8bc2-4649-8a55-e264376a76c3)

 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
$ ./argshift.sh 1 2 3
 ![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/ae2aad02-31d5-4d75-ba3b-a8a83cf8ac38)

 cat argshift1.sh
```bash
 #/bin/bash 
 # store arguments in a special array 
args=("$@") 
# get number of elements 
ELEMENTS=${#args[@]} 
 # echo each element in array  
# for loop 
for (( i=0;i<$ELEMENTS;i++)); do 
    echo ${args[${i}]} 
done
```
$ chmod 777 argshift.sh
## OUTPUT
$ ./argshift.sh 1 2 3
 
cat argshift.sh
```bash
#!/bin/bash 
set -x 
while (( "$#" )); do 
  echo $1 
  shift 
done
set +x
```
## OUTPUT
 ./argshift.sh 1 2 3
 ![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/cfe4ebff-ef95-469e-a264-7ca5ec657f73)

 
cat > nc.awk
```bash
BEGIN{}
{
print len=length($0),"\t",$0 
wordcount+=NF
chrcnt+=len
}
END {
print "total characters",chrcnt 
print "Number of Lines are",NR
print "No of Words count:",wordcount
}
 ```
cat>data.dat
```bash
bcdfghj
abcdfghj
bcdfghj
ebcdfghj
bcdfghj
ibcdfghj
bcdfghj
obcdfghj
bcdfghj
ubcdfghj
```
awk -f nc.awk data.dat
## OUTPUT 
 ![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/15679555-6a18-43d0-946e-216d3cb956e7)

cat > palindrome.sh
```bash
#num=545
echo "Enter the number"
read num
s=0
rev=""
temp=$num
while [ $num -gt 0 ]
do
	# Get Remainder
	s=$(( $num % 10 ))
	# Get next digit
	num=$(( $num / 10 ))
	# Store previous number and
	# current digit in reverse
	rev=$( echo ${rev}${s} )
done
if [ $temp -eq $rev ];
then
	echo "Number is palindrome"
else
	echo "Number is NOT palindrome"
fi
```
## OUTPUT 
![image](https://github.com/Hariveeraprasad-2006/OS-Linux-commands-Shell-script/assets/145049988/b2bc87cb-a90b-4f4a-8bda-5d90ba03b38d)


# RESULT:
The Commands are executed successfully.

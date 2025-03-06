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
![Screenshot from 2025-03-05 20-42-11](https://github.com/user-attachments/assets/b254fcf7-5e57-46d4-85c8-f9a7f2d8b3cb)

cat < file2
## OUTPUT
![Screenshot from 2025-03-05 20-43-37](https://github.com/user-attachments/assets/bb50636d-ef7b-444d-8360-40fc9fa950ca)

# Comparing Files
cmp file1 file2
## OUTPUT
![Screenshot from 2025-03-05 20-46-16](https://github.com/user-attachments/assets/be2f6a5c-ee2a-44cd-9ff3-517ed97f9512)

comm file1 file2
 ## OUTPUT
 ![Screenshot from 2025-03-05 20-49-33](https://github.com/user-attachments/assets/9415f21d-12aa-4c38-a472-7649d0e9cbec)

diff file1 file2
## OUTPUT
![Screenshot from 2025-03-05 20-50-54](https://github.com/user-attachments/assets/12363060-d29f-4861-81b8-03de1e7873a0)

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
![Screenshot from 2025-03-05 20-59-28](https://github.com/user-attachments/assets/ae04e831-4e0e-41e9-9666-3a7d8ef5e078)

cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2025-03-05 21-03-14](https://github.com/user-attachments/assets/f8ba7a39-58a6-4bc1-9722-c3ab95fb286a)




cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2025-03-05 21-04-25](https://github.com/user-attachments/assets/9b455fd4-708b-4b2e-a919-17c4be392f55)



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

![Screenshot from 2025-03-05 21-27-24](https://github.com/user-attachments/assets/c4f90da3-b963-4762-b52c-30f808df7acb)


grep hello newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/b16a8ae1-2cef-4e43-b4f8-87a9d8f1537b)



grep -v hello newfile 
## OUTPUT
![Screenshot from 2025-03-06 17-37-23](https://github.com/user-attachments/assets/ea36f36b-de1d-41cb-bd83-95df92598cd0)

cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/390cf527-eaa3-451e-b16a-481bea3a58ff)


cat newfile | grep -i -c "hello"
## OUTPUT
![image](https://github.com/user-attachments/assets/e4ea6103-9836-4295-b375-41de2fa3a3da)

grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/user-attachments/assets/d4b481bd-6c3c-4829-bee3-8b2199473980)

grep -w -n world newfile   
## OUTPUT
![image](https://github.com/user-attachments/assets/a0e12fbe-d5de-401a-a6d8-bcec1fcec38d)


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
![image](https://github.com/user-attachments/assets/fe1c2349-33f8-411c-b234-de0ef3900e9d)




egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/802f352c-6fe7-4dd0-99d6-c3141c20d600)

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/910e0902-1a68-403c-8721-d9a385aee794)




egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/57b071c0-7585-4503-8f91-9d59483af3dc)



egrep '(world$)' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/d174375b-6c03-4e55-a53e-43ac6343986e)


egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/858794c3-d6da-491c-b3a5-c4f924759669)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/1fb5c466-36ac-4a6b-abf6-10f542f69dac)

egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/b40e8e70-f5be-417c-b309-7ba8d21887b2)



egrep 'Linux.*world' newfile 
## OUTPUT

![image](https://github.com/user-attachments/assets/324297e5-22e2-4fc2-8ab6-cd7e453b5188)

egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/user-attachments/assets/f69141ec-2b56-4f5b-a313-200b9fb016bf)



egrep l{2} newfile
## OUTPUT
![image](https://github.com/user-attachments/assets/4a11a4d7-1570-49e7-ad53-ec7ebd994c14)




egrep 's{1,2}' newfile
## OUTPUT 
![image](https://github.com/user-attachments/assets/49a7be52-e3a3-425c-9679-e31b70b3afa9)


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
![image](https://github.com/user-attachments/assets/01c2ce50-6a4c-46d6-834a-949cb72286e1)




sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/0b339dff-2e2a-4f19-849f-e1b21a5945ff)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/f5ac1d0b-1662-46b8-b3a5-7d2b7005f59c)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/237aed3c-7264-4dbd-8ccc-9dcc0336b7ba)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/0a98ff46-3856-4637-a0a5-4d7ae36debe3)



sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/d9a28c78-f45a-469b-88c2-bd8a12d72212)




sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/885be8cb-c4f6-4c37-9047-2834ba9e8abf)





sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/user-attachments/assets/34b3ea7f-99b0-4097-8551-cf26e6a1a4e3)



seq 10 
## OUTPUT
![image](https://github.com/user-attachments/assets/d3769fd2-3100-4455-9e65-63c403edcccf)




seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/user-attachments/assets/5b62e901-3d90-4f5b-b7a6-b5f815013e1f)


seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/user-attachments/assets/e1121883-60b9-4c32-bd14-5b3829afd580)



seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/270cdf5f-eae5-405f-b915-41d7c293520c)




seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/f5440c20-3d1e-4bb3-a66d-f74bfba34ad6)



seq 10 | sed '2,9c hello'
## OUTPUT
![image](https://github.com/user-attachments/assets/1caa4449-e608-4316-8597-6fc80b180d74)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image](https://github.com/user-attachments/assets/b007a0ef-4d88-468f-820c-c1936964676f)


sed -n '2,4{s/$/*/;p}' file23
![image](https://github.com/user-attachments/assets/e9a719ca-4700-4a24-a962-97bdca201b5a)


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
![image](https://github.com/user-attachments/assets/06a7c4ee-f343-47c4-875c-02c1ecceafa9)



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

![image](https://github.com/user-attachments/assets/fb5b97fc-0485-47f4-9307-dceb187328f7)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image](https://github.com/user-attachments/assets/7d843b3f-0bea-4beb-a7ac-b2cb7b312847)





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
![image](https://github.com/user-attachments/assets/d31f7927-5c0d-42c8-b654-44899cab1a8a)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/user-attachments/assets/f9150990-6a59-43c3-8c12-c0eb5774a1b7)




#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/user-attachments/assets/9e4d55a3-3322-4278-a256-610e098b59db)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image](https://github.com/user-attachments/assets/308a0c44-68b4-4de0-8cab-eb5346ec1fb6)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![image](https://github.com/user-attachments/assets/a6a9f543-a36e-4918-9d95-9c769047fa7a)



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
![image](https://github.com/user-attachments/assets/814a1e65-8dba-43a3-87c0-e44d547c930a)

ls file1
## OUTPUT
![image](https://github.com/user-attachments/assets/f96597e2-e6e9-44a9-8285-07bbce11becc)


echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/c2a82731-cf3c-41ec-b817-41940b6242a8)


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image](https://github.com/user-attachments/assets/b5d64f44-6b36-4cdb-bdaa-86b12ed3f96c)



 
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
![image](https://github.com/user-attachments/assets/6a97f207-4338-4f4b-92e1-5fe8276decfc)


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
![image](https://github.com/user-attachments/assets/bb2078f2-4c18-4078-a8ef-02b2301dd0b5)




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
![image](https://github.com/user-attachments/assets/b0fc6475-2879-4d92-bcee-414838c4415c)


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
![image](https://github.com/user-attachments/assets/7e68ca4b-c31a-42cd-9b00-904a7c827ad6)



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

![Screenshot from 2025-03-06 19-19-41](https://github.com/user-attachments/assets/5d0ae75c-5c02-4919-b9a4-0276647893d5)




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

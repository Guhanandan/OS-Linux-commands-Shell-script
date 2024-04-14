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
![312823451-0119401d-8e53-42c4-ab54-ce749dc6a03e](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/c0d2c4cf-ca7a-4e9f-8189-8c90a4fc8c95)



cat < file2
## OUTPUT
![312823636-9d6b43a7-9146-4ad3-bd12-6124400fb4d7](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/6024576f-a277-4b1e-bd0f-ba01a4d04636)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![312824286-ec7146a1-7dcf-4519-b2bd-bb074874a9f6](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/a8fd3aaa-b543-4d4f-9982-2f86387ff46d)

comm file1 file2
 ## OUTPUT
![312824209-2b388c18-8716-471f-86a5-104b81593a8b](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/a8bb07ed-3dad-4e9d-8fa9-fc153960ac6c)

 
diff file1 file2
## OUTPUT
![312824501-bdc3e442-d591-40aa-b92a-121299adbb65](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/42c32117-62b8-48e4-a584-b6fe8205ec6a)



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
![312824664-141e89e4-c3d8-4296-b12d-a2e6bb80f2df](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/60e400f4-69bc-4705-8796-e839e421ebd2)



cut -d "|" -f 1 file22
## OUTPUT



cut -d "|" -f 2 file22
## OUTPUT
![312824777-b1f5d32d-f1a3-4a66-9c0e-10d02548f316](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/87924b71-cc47-4556-b88f-9da1d39c38e7)


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
 ![312823117-fc26c416-54b1-4b9c-b839-1e6a77c2ff12](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/ed173e26-0703-4012-9c30-1b40f4d6d0bb)


grep hello newfile 
## OUTPUT
![312825332-3cfe2166-0ee0-46f4-9b7c-44512aeae4cd](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/c3856cc7-dabc-4192-9df4-9f924e38d5a5)




grep -v hello newfile 
## OUTPUT
![312825594-d6dd2db3-b402-47b5-84f7-35e3b2038e37](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/3dcfe6f8-378e-4fe7-87f5-c6fbf9534055)



cat newfile | grep -i "hello"
## OUTPUT
![312826766-3c2aa26a-270d-42cf-9f04-ce10dc341942](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/ad8858a5-a8a3-404d-a1bf-01f5f1b09ccc)




cat newfile | grep -i -c "hello"
## OUTPUT
![312826766-3c2aa26a-270d-42cf-9f04-ce10dc341942](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/aaacf885-889b-4562-b29c-1a5182e7049b)




grep -R ubuntu /etc
## OUTPUT
![312827082-04c00dca-5051-48a8-9333-c20a7bfd9328](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/f064034f-772d-4349-813f-f9560ab3c4a9)



grep -w -n world newfile   
## OUTPUT
![312827384-a08e3266-9005-4680-b75a-cb7687d0b869](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/7394fde4-ed9b-4fde-b202-aa5697e7c8ea)


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
![312830227-2e1abf54-ea02-4eb8-b1f6-fff5fef677e0](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/e7a17f23-a45f-4668-bd2e-aaf2168c87af)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![312830407-618c12f7-7069-417f-8616-481edb3859ad](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/ba6b1a95-a771-4966-a12c-a68dc78628e4)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![312830642-cc45623c-2d8c-40a7-901e-488b36d5ed02](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/11ba95ac-306f-4986-b15f-169e81557747)




egrep '(^hello)' newfile 
## OUTPUT
![312830907-b44ed469-befa-4fb3-a15e-41324eaca2dc](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/d61ed6f8-1e17-4ae8-933e-2a9b0469d123)



egrep '(world$)' newfile 
## OUTPUT
![312831337-705b8878-2407-4f14-b7ec-1a92f9a81314](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/e974942f-29bd-4f71-92ad-be5042d1206b)



egrep '(World$)' newfile 
## OUTPUT
![312831486-740a21f7-daab-4ba2-8a61-4c282f7e7766](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/02138eb9-7988-4421-a999-0a5d71f9a7fb)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![312831660-25ac512f-2dfb-4038-925f-0b2818d8a912](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/eb86018a-c86a-43ae-8ca8-c21f304a09c5)



egrep '[1-9]' newfile 
## OUTPUT
![312831851-27139ca7-cf2a-4851-8047-cd30f39b3da4](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/e3703e78-f3b9-44b2-aa9c-69896b86793c)



egrep 'Linux.*world' newfile 
## OUTPUT
![312832122-65f9c469-4f04-4490-b7b8-75268e22fbce](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/c95d2f00-22d1-4eda-8d9d-2682704e556d)


egrep 'Linux.*World' newfile 
## OUTPUT
![312832282-82dd6efa-a158-4a99-b1d3-60ec8d16d18c](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/3353177b-70ac-45ac-8a95-ce9b7fdf0ba7)


egrep l{2} newfile
## OUTPUT
![312832569-7878b983-dcc0-4fad-96df-0eabfaff7a9c](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/aa803006-de39-48a1-9189-aabb1bf52eaf)



egrep 's{1,2}' newfile
## OUTPUT 
![312833039-5743baa7-5209-46b3-89ff-1398ce18f46d](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/d7794a1e-fbbf-42b9-86bc-25c3541b6fb7)


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
![312890522-6ea57d36-ce6c-4daf-8d42-39476d4518a4](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/5fba16f7-5442-4ac8-a9d5-03c914fa1461)



sed -n -e '$p' file23
## OUTPUT
![312890691-ecf7119f-656f-4dfe-89fa-6e49e0f9104c](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/5b8af7c7-c6ba-4099-9ec6-140937eb1dc8)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![312890912-677587a1-2033-4bcc-8394-4e7253d8906c](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/4e449c05-e1b1-4bb8-8764-bf3ad7f32bb1)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![312891134-b00debdd-71b6-4595-8af4-8dd502d1e9d1](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/4e8e8a9f-d7f2-4ce6-bcfd-0d3d1844582a)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![312891478-8f6fb32f-68c3-4685-8377-895403873fdf](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/5ab72b63-bcf3-41ed-a4ac-9a4569f95695)



sed -n -e '1,5p' file23
## OUTPUT
![312891653-a57f600b-bf98-4ccf-8ea3-c966a7e7097c](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/e95908bd-a399-4205-8fa6-188d31049967)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![312892738-65246582-bd0f-490b-8352-01ff92960b8f](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/c0fc11b1-6d8b-485d-ae2c-a2b267b33416)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![312891961-ca015e97-51d3-46b3-a4b2-883386487e96](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/ba8214dd-21db-4a3b-ac8b-b125f7ab37a6)



seq 10 
## OUTPUT
![312892165-d89684e2-6e84-4c92-b8f7-05a1c425b8f6](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/d5e60629-43f0-4ed2-ae57-81cdd5107916)



seq 10 | sed -n '4,6p'
## OUTPUT
![312892951-f2346439-9a61-4e57-a9fb-66a7fe066be9](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/ee9c7cc1-3545-4938-a031-a3fd01e0a9c2)



seq 10 | sed -n '2,~4p'
## OUTPUT
![312893365-782ae142-f59f-4252-a128-61f12027a343](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/af8b0178-6c24-420b-b38c-fae52343eb94)



seq 3 | sed '2a hello'
## OUTPUT
![312893553-a198c8b4-6c65-4fe9-ba15-3b9106f603af](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/841916e0-86ae-4eb8-923a-b04e89c7fc4e)



seq 2 | sed '2i hello'
## OUTPUT
![312893738-cc2be9dc-529d-48a8-8006-8d9658906ac7](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/95aafc2a-a839-4a6e-89c0-cab1960a6cb3)


seq 10 | sed '2,9c hello'
## OUTPUT
![312894013-1ff68b19-cd1a-4152-930d-191cdf0a400a](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/5e682b1e-3cf5-46e7-a378-051266345010)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![312894616-26180a7a-ef81-4172-b7aa-275a1a5545b3](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/57a5f5f8-64e1-4a14-95e2-70a007de3846)



sed -n '2,4{s/$/*/;p}' file23


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
![312894885-4082ae2d-91db-4998-95a9-336e7a63e3e4](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/af1de482-387b-4599-8020-91dadecb1463)


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
![312896921-924b5e4f-b6d9-4ce3-894b-2b1edbf587c0](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/1b3e7031-4894-46f4-9fea-e511966233d2)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![312897587-94e1fa19-3646-4f72-97c8-eff4a0e11279](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/d6b5912a-6050-4f07-baff-089e1ac81303)

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
![312898870-de7ce8af-1855-4dec-99f3-734859a20a00](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/b9e157ed-7452-408b-ac15-64f052515b6a)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![312899242-255942df-5e83-4d32-b128-ee2fe540cebe](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/30937172-7c97-412e-9153-0e87172ae09e)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![312900431-8c62851c-a964-43f2-86cc-74216fecdaf3](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/bdd14e41-c796-44e7-ad89-064b7b122d91)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![313092740-3eb2f341-b2a9-463b-9314-97f5a3971a76](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/df326d3f-bf2d-4390-87f8-cb4c0a55519b)


tar -xvf backup.tar
## OUTPUT
```
x file1.txt
x directory1/
x directory1/file2.txt
x directory1/file3.txt
```
gzip backup.tar

ls .gz
## OUTPUT
```
 backup.tar.gz
```
gunzip backup.tar.gz
## OUTPUT
```
backup.tar
```
 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![307824234-cd6aa88e-aa03-4879-8eac-096a80a8bf1a](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/d05d40ba-a176-40e0-ba4f-e8f1655fe051)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![307824796-7449297d-09c9-4e47-9593-2a2ae75545ea](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/14708e6e-cab9-48dd-bf94-48f5b4245e9c)


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
```
File name is ./scriptest.sh
File name is scriptest.sh
First arg. is 1
Second arg. is 2
Third arg. is 3
Fourth arg. is
The $@ is 1 2 3
The $\# is $#
The $$ is 124
```
 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![307825432-c2ffd586-64f4-4d86-814f-53fd3b966af5](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/c4712f0e-e08e-40e7-bbda-a9323f2e4553)

 
abcd
 
echo $?
 ## OUTPUT
![307826499-e004d6ed-48ab-45a6-bfd8-ab8faa8788b5](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/6a9916a6-c77d-463a-a012-5ed4a88eca57)


 
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
##OUTPUT
![307828678-669c08af-be10-452a-a16b-2d960c674987](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/c3cb96dc-f16e-4623-b806-2e176fc48cee)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
```
baseball is less than hockey
```

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
./psswdperm.sh
## OUTPUT
```
You are the owner of the /etc/passwd file
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
![307832276-efa998fe-2806-4eca-ace7-1d71dda33cf6](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/4c6e55e8-469c-4848-aa64-1dea89c8d762)



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
##OUTPUT
![307833052-545398c0-2c77-4e44-b53a-6ef098142c6f](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/0f6d974a-c275-4bad-a666-bb196fd058e5)

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

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
![307833801-3f9abd70-a9ff-43f5-9b46-39fd1f374d55](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/98dbfab5-99d6-40f9-adda-44138a64559d)

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
![307834688-73bf26c3-76c2-4dbe-8aa4-213a1cef52fb](https://github.com/Guhanandan/OS-Linux-commands-Shell-script/assets/100425381/dd87dd11-98cf-4710-a7a4-82b689fd77ff)


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
```
Welcome Ram/Rahim
Please enjoy your visit
Special testing account
gganesh, Do not forget to logout when you're done
Sorry, you are not allowed here
```
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

## OUTPUT


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
```
Visit beautiful Hyderabad
Visit beautiful Alampur
Visit beautiful Basara
Visit beautiful Warangal
Visit beautiful Adilabad
Visit beautiful Bhadrachalam
Visit beautiful Khammam
```
cat forctype1.sh 
```bash
#!/bin/bash
# multiple variables
for (( a=1, b=5; a <= 5; a++, b-- ))
do
echo "$a - $b"
done
```
$ chmod 755 forctype.sh
$ ./forctype1.sh 
## OUTPUT
```
The value of i is 1
The value of i is 2
The value of i is 3
The value of i is 4
The value of i is 5
```
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
```
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
```
1 - 5
2 - 4
3 - 3
4 - 2
5 - 1
```
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
```
Iteration number: 1
Iteration number: 2
Iteration number: 4
Iteration number: 5
The for loop is completed
```
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
```
Enter your name: John
Hello John, welcome to my program.
```

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
```
Enter your name: sanju
Hello sanju, welcome to my program.
```


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
```
$ bash script.sh 1 2
The result is 2
```
 
 ./funcex.sh 1 2

 
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
```
1
2
3
```
 
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
```
1
2
3
```
 
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
 ```
total characters 75
Number of Lines are 10
No of Words count: 10
```
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
```
Enter the number
121
Number is palindrome
Enter the number
69
Number is NOT palindrome
```

# RESULT:
The Commands are executed successfully.

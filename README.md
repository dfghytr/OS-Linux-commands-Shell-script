
## Operating systems Lab exercise
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
![os1](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/352ba4b2-72d4-4aaf-bc03-90828f3d9eb3)



cat < file2
## OUTPUT
![os2](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/1f053c25-eeee-4256-9d9f-ae94ffde7ada)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![os3](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/6359b1c7-927d-4f6e-82d0-21c8e4f6203c)

comm file1 file2
 ## OUTPUT
![os4](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/a88c9c69-1a69-483d-ba74-a4e2949aa760)

 
diff file1 file2
## OUTPUT
![os5](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/24216d87-20e1-40a4-a019-8c03517b843c)


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
![os6](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/6ef52174-4dbf-47ce-91fe-c07b3a3a959a)




cut -d "|" -f 1 file22
## OUTPUT
![os7](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/1c337b38-e287-43de-a04b-0f6f7bdd69d0)



cut -d "|" -f 2 file22
## OUTPUT
![os8](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/5c0eed3d-0d0b-4f10-9240-1fd1b635832c)


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
![os9](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/f189138b-e979-45c7-827d-d118b77fca8c)



grep hello newfile 
## OUTPUT
![os10](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/9a181763-eca2-42fe-b40d-95776e629348)




grep -v hello newfile 
## OUTPUT
![os11](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/0f464155-602d-4009-9bf9-645159fa0fe7)



cat newfile | grep -i "hello"
## OUTPUT
![os12](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/ab548556-ee9b-43b6-afd1-45dfbe5ca4e3)




cat newfile | grep -i -c "hello"
## OUTPUT
![os13](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/8355b036-756b-4f39-94cc-d7e953a6fef4)




grep -R ubuntu /etc
## OUTPUT
![os14](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/ef2bb01e-9525-4eee-bf05-74375b421f2a)



grep -w -n world newfile   
## OUTPUT
![os15](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/c5813271-8ae0-4022-9ed0-d38c8c067856)


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
![os16](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/1938b1e6-6213-4db6-9048-4c93145044cc)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![os17](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/3c665971-1e94-4b5c-ad82-04f913fd5047)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![os18](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/abc80b74-31e7-41db-aa4c-66fcbeb2a207)




egrep '(^hello)' newfile 
## OUTPUT
![os19](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/4c9058ae-804c-457a-b271-2fea0c42bc34)



egrep '(world$)' newfile 
## OUTPUT
![os20](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/9b837e61-09f3-4c93-8597-3b25315fd8e9)



egrep '(World$)' newfile 
## OUTPUT
![os21](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/ae792910-fc0b-4e03-87c4-f4a44439037a)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![os22](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/6e628084-c754-490a-b937-0c49aec60ce1)



egrep '[1-9]' newfile 
## OUTPUT
![os23](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/f595db99-1e28-4880-8972-a8ea6385c6a9)



egrep 'Linux.*world' newfile 
## OUTPUT
![os24](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/31b8d33e-57aa-4dbd-b52a-b1c586f7615e)


egrep 'Linux.*World' newfile 
## OUTPUT
![os25](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/acf88b37-7d8d-4c27-bdbf-699d9d27272c)


egrep l{2} newfile
## OUTPUT
![os26](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/f3d3e2af-5c9d-45e7-b398-a0109c4224b1)



egrep 's{1,2}' newfile
## OUTPUT 
![os27](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/9d9123a7-c8fd-440c-94ad-d402bb3c3549)


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
![os28](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/cd6648a5-3b1d-4f6d-8122-279d36aeb72b)



sed -n -e '$p' file23
## OUTPUT
![os29](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/626c4bc2-2c35-42d7-8f6c-033340a9f7de)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![os30](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/bd80d5dc-1f79-40b1-ace4-5802c9ed54a2)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![os31](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/18515c40-e8c8-4609-91bb-1dd4623f7b48)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![os32](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/2a09c631-6ad1-4995-9caa-c5d0ffdd0cb2)



sed -n -e '1,5p' file23
## OUTPUT
![os33](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/adcb0ed0-af34-469a-8dde-0397abefa44c)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![os34](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/43b7eac1-894c-435d-8334-631dd2f4a6a7)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![os35](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/e735d24c-c9a1-4591-96a2-ab77929509d0)



seq 10 
## OUTPUT
![os36](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/f1f6ced6-d0fe-47bc-907f-50334f58b0a3)



seq 10 | sed -n '4,6p'
## OUTPUT
![os37](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/8cb43fa9-6fc9-42d7-935b-911e85442d70)



seq 10 | sed -n '2,~4p'
## OUTPUT
![os38](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/e92117ed-8830-48f4-8089-a4c086438488)



seq 3 | sed '2a hello'
## OUTPUT
![os39](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/0475362f-fb37-4d2b-8730-4a15bca23023)



seq 2 | sed '2i hello'
## OUTPUT
![os40](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/fc09c814-85f6-4284-bdbe-ec64e10f7a42)


seq 10 | sed '2,9c hello'
## OUTPUT
![os41](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/44539eb7-4e1f-4c1a-adea-69d3d35f14a1)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![os42](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/6b94678b-c036-4727-b2bf-fe97144c40b7)



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
![os43](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/66ac8770-49c7-4647-975b-ab411b70ba4b)


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
![os44](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/17ee2681-ba24-4f3a-9c87-ed77f3543773)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![os45](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/0cb80fc5-a699-4683-9fed-d79a4cb49deb)

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
![os46](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/8ca8897a-9f7e-4c82-b54c-e8389dc4c305)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![os47](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/bf7f2f25-59cb-4207-91b8-109421cb1d4b)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![os48](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/a720dd43-dcc5-4c16-8f6f-64b763ce3ced)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT
![os49](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/51589f1f-9ab3-4056-9ac2-cde4555d88ff)


tar -xvf backup.tar
## OUTPUT
![os50](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/c1b6f343-2f20-4309-af69-60e444083e05)

gzip backup.tar

ls .gz
## OUTPUT
 ![os51](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/21572c29-2fd0-41e4-8eef-721dea92e51d)

gunzip backup.tar.gz
## OUTPUT
![os52](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/9395f07f-fd55-4c6e-aa58-6d49e23eeb47)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![os53](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/5f94d577-0cc9-42cc-859a-7713ef96b1a0)

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![os54](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/30d8db27-7127-4a00-8f4a-98b37e750f7b)

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
![os55](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/b30ea6ce-250b-4a79-9cc6-3bb09f513902)

 
ls file1
## OUTPUT
![os56](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/4952fcb7-9959-47a3-92a7-c1be2ed6a987)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
![os57](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/be5a08c3-62db-4b35-84cc-79ddd375d5be)

echo $?
## OUTPUT 


abcd
 
echo $?
 ## OUTPUT

 
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
![os58](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/20d146a4-258b-4a5e-a3e6-a6b881395986)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![os59](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/7f6d4758-a76a-4453-8f52-bf205319a7e6)


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
![os60](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/4844a78e-221d-4257-b245-e1416c6f4261)

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
![os62](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/089f47a3-2ac6-4e7b-9a78-6100f5799ae4)




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
![os61](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/903b9b01-e65c-4ff9-b773-495235216887)

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
![os62](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/eb617274-6212-4e0f-9b2d-b2dda49dcbe1)

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
![os63](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/54952ecb-9b3d-4297-b957-1efa2fdc3e61)


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
![os64](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/d0862b95-f596-43a7-8a0f-0817c411875c)

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
## output
![os65](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/1f8f5357-4cb8-4b09-b437-4b62f8a75917)

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
 ## output
 ![os66](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/03accf7a-09f9-4a9d-966f-6190786536a7)

 
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
## output
![os67](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/41690f9f-e3cc-4680-90a5-d5d72fe952e2)

 
 
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
## output
![os68](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/3247aed0-b096-4f31-89e0-87abc45d2ae6)

 
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
 ## output
 ![os69](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/0bab3a5f-d1ac-48f0-8690-12114bd75806)

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
 ## output
 ![os70](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/a7176669-99fe-4173-89bf-5a1a447f77a9)

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
![os71](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/8786ca9c-5a69-4377-afe3-9de89ebe2888)


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
![os72](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/5fb4ac38-9ec5-47da-9c85-1fc036a5b7f7)

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
![os73](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/0182b56c-b459-4d0a-bd0a-8c34b7e7b262)

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
![os74](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/c5831236-f9b9-40ef-ba31-3a7858402cfd)

 
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
![os75](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/2bd565f5-1398-4c9b-a2af-e20267e57556)

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
![os76](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/7c786f86-fb30-46f8-8b62-a12c6be16c0c)
 
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


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: RIYA P L"
echo "Hello RIYA P L, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![os78](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/bdb8cdc2-bc96-4f9c-a297-852a731aa970)



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

 
 ./funcex.sh 1 2
![os79](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/c05e735c-8313-4989-bfcd-eefe8587785c)

 
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
![os80](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/13348ac1-2c3a-43e3-817f-250cd86400ab)
 
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
![os81](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/a4ab1f9d-7751-4a61-88f3-c31d5249e10f)
 
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
![os82](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/77e82648-c31c-489c-8bd5-5c9c1c94b880)
 
 
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
 ![os83](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/04799b44-e6a5-42d3-9851-db7fd07243dd)

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
![os84](https://github.com/23005672/OS-Linux-commands-Shell-script/assets/138971519/4bc48e38-b185-4ed4-9bf9-a4df06e348f3)


# RESULT:
The Commands are executed successfully.

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
<img width="631" height="217" alt="image" src="https://github.com/user-attachments/assets/6744a9b1-3ddf-4b53-ae82-010d35674cd6" />



cat < file2
## OUTPUT
<img width="782" height="327" alt="image" src="https://github.com/user-attachments/assets/4a9f5af1-0a54-48a3-8bb2-75bcfe9808d7" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="730" height="216" alt="image" src="https://github.com/user-attachments/assets/dd0ca1dd-d5d9-4629-9111-996c5fd0a5a5" />

comm file1 file2
 ## OUTPUT
<img width="601" height="377" alt="image" src="https://github.com/user-attachments/assets/80a3c237-a3da-42c3-a057-e1a41748b8fa" />


 
diff file1 file2
## OUTPUT
<img width="402" height="275" alt="image" src="https://github.com/user-attachments/assets/9339e109-4eb2-4520-806b-0c443221a91c" />


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

<img width="505" height="102" alt="image" src="https://github.com/user-attachments/assets/4c65198c-e014-4b35-8167-419bba1c4358" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="520" height="127" alt="image" src="https://github.com/user-attachments/assets/c764252a-e0b6-4e8b-bec6-f560c1afc53e" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="525" height="122" alt="image" src="https://github.com/user-attachments/assets/5ba27a14-48e0-4dcb-bd64-33f562b2f0f3" />


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
<img width="592" height="102" alt="image" src="https://github.com/user-attachments/assets/0d2db7b2-6854-460f-bb98-14d5dc60bb77" />



grep hello newfile 
## OUTPUT
<img width="567" height="72" alt="image" src="https://github.com/user-attachments/assets/7034e115-5719-40d4-a980-92a4fba0b91e" />




grep -v hello newfile 
## OUTPUT
<img width="537" height="72" alt="image" src="https://github.com/user-attachments/assets/038c7dcb-815c-44d2-9a0b-04508cdd4308" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="602" height="96" alt="image" src="https://github.com/user-attachments/assets/8c67a4d2-c4ff-4f2a-a627-2b1058e98eda" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="520" height="75" alt="image" src="https://github.com/user-attachments/assets/27179b57-b2c6-417b-acb9-bb5cf4b609e6" />




grep -R ubuntu /etc
## OUTPUT
<img width="837" height="566" alt="image" src="https://github.com/user-attachments/assets/57dd8dfd-7327-434a-ae80-684850640727" />



grep -w -n world newfile   
## OUTPUT
<img width="427" height="102" alt="image" src="https://github.com/user-attachments/assets/544db536-58fa-44f6-b2d0-d2a42aad59f9" />


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
<img width="502" height="97" alt="image" src="https://github.com/user-attachments/assets/d79dfbec-af24-41db-927a-b93bfa545e42" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="510" height="102" alt="image" src="https://github.com/user-attachments/assets/9a854207-db7d-4dcd-a41c-3d6336380832" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="556" height="96" alt="image" src="https://github.com/user-attachments/assets/00419dc2-2035-4b66-b430-06150f1e0eef" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="580" height="72" alt="image" src="https://github.com/user-attachments/assets/a94677c3-3540-4951-ad86-496e668a41dc" />



egrep '(world$)' newfile 
## OUTPUT
<img width="650" height="97" alt="image" src="https://github.com/user-attachments/assets/867cd6a5-f0d8-4c32-8de0-2c983ac0897e" />



egrep '(World$)' newfile 
## OUTPUT
<img width="731" height="77" alt="image" src="https://github.com/user-attachments/assets/7a08613b-6080-4b82-b244-cd1778b69f07" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="596" height="142" alt="image" src="https://github.com/user-attachments/assets/b2ea55c2-be8c-49f5-bdfd-ce10b194cd3b" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="705" height="81" alt="image" src="https://github.com/user-attachments/assets/0c4b468c-cbd4-42f0-919c-0350887eb65d" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="537" height="70" alt="image" src="https://github.com/user-attachments/assets/2096a494-8cdd-430c-b911-d42f498dd2cf" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="615" height="62" alt="image" src="https://github.com/user-attachments/assets/b1a4695b-6e43-4fb1-b53c-7024cdba4ba1" />


egrep l{2} newfile
## OUTPUT
<img width="636" height="97" alt="image" src="https://github.com/user-attachments/assets/51a314b8-7a01-42a5-9c68-d2437822c164" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="637" height="126" alt="image" src="https://github.com/user-attachments/assets/c18f416e-ef1f-4650-b284-6a53541955f9" />


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
<img width="432" height="77" alt="image" src="https://github.com/user-attachments/assets/bac09ea8-1052-4d11-b55e-9f4212c3fb31" />



sed -n -e '$p' file23
## OUTPUT
<img width="395" height="77" alt="image" src="https://github.com/user-attachments/assets/32ee833f-232b-420c-908f-99ed06a78a14" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="402" height="247" alt="image" src="https://github.com/user-attachments/assets/e7be954a-bd2a-4cd2-be60-e3a67e506a9e" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="447" height="251" alt="image" src="https://github.com/user-attachments/assets/d7745294-1687-4a16-86ee-888cd2ef4233" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="492" height="246" alt="image" src="https://github.com/user-attachments/assets/9ac8e677-48bd-4490-8970-0211cc9658db" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="462" height="176" alt="image" src="https://github.com/user-attachments/assets/8ac7fa1a-767a-4c88-9ad4-8f205c4bc8f6" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="447" height="127" alt="image" src="https://github.com/user-attachments/assets/83324a54-6695-40d5-9485-b1f77c8b09f0" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="530" height="101" alt="image" src="https://github.com/user-attachments/assets/99d8312f-9bf5-4494-a0a4-8c2aebc18c67" />



seq 10 
## OUTPUT
<img width="475" height="292" alt="image" src="https://github.com/user-attachments/assets/86e501d0-997f-40f2-ba69-2ce01a5ab650" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="462" height="132" alt="image" src="https://github.com/user-attachments/assets/42f3be8d-a3ff-4b2c-a05e-0f7e6d6ba384" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="492" height="127" alt="image" src="https://github.com/user-attachments/assets/c6a56fba-eefa-4a3e-a154-92d776487397" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="467" height="147" alt="image" src="https://github.com/user-attachments/assets/adb902fb-a9f9-4948-87c9-7092bfef205a" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="407" height="122" alt="image" src="https://github.com/user-attachments/assets/ae9729e3-6bbb-4bc7-a6f3-1e170f89ce20" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="397" height="127" alt="image" src="https://github.com/user-attachments/assets/fa9b6978-50e8-4011-a526-0b5b34028d73" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="422" height="122" alt="image" src="https://github.com/user-attachments/assets/0534cc7a-e3d0-471c-883f-7eb81c8fbf5e" />



sed -n '2,4{s/$/*/;p}' file23

<img width="517" height="135" alt="image" src="https://github.com/user-attachments/assets/dce7bae4-5adb-4f5e-b2a6-d85a6ec0c7f5" />


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

<img width="427" height="152" alt="image" src="https://github.com/user-attachments/assets/d2e8be56-3c5c-42fc-90ac-2d8437f757ee" />


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


<img width="560" height="312" alt="image" src="https://github.com/user-attachments/assets/0eb01de6-6f00-4194-91a9-e89555bf0614" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="557" height="247" alt="image" src="https://github.com/user-attachments/assets/33bfef01-99d1-4767-993b-47670e21dacc" />

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

<img width="430" height="130" alt="image" src="https://github.com/user-attachments/assets/ade3ed10-4c55-4866-a905-b5b93cf05b8c" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="567" height="122" alt="image" src="https://github.com/user-attachments/assets/c338eb62-e47d-4a51-911b-9a0cab28ea2b" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="557" height="570" alt="image" src="https://github.com/user-attachments/assets/abeefe25-06d5-4f49-b148-3ccefb85ee5e" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="750" height="600" alt="image" src="https://github.com/user-attachments/assets/7291f15f-39ab-43cf-98e3-4cc2bc29c3e1" />


tar -xvf backup.tar
## OUTPUT

<img width="510" height="542" alt="image" src="https://github.com/user-attachments/assets/d7fc6aa0-4c08-4c31-b6a7-b29a6e4dfbe7" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="445" height="72" alt="image" src="https://github.com/user-attachments/assets/6f16633a-72b6-4ba9-b238-207f1b6311f4" />

gunzip backup.tar.gz
## OUTPUT

<img width="470" height="52" alt="image" src="https://github.com/user-attachments/assets/c5924aa6-3b61-43ee-a206-c6b73e021b26" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="531" height="150" alt="image" src="https://github.com/user-attachments/assets/4842338f-6145-421d-86bb-a2b269fe87dc" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="435" height="172" alt="image" src="https://github.com/user-attachments/assets/7ba3e202-5b1f-4f28-a128-aabc2f0a586d" />


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

<img width="682" height="442" alt="image" src="https://github.com/user-attachments/assets/c9242ecf-fd73-4b26-b4f6-254278850b92" />

 
ls file1
## OUTPUT

<img width="286" height="72" alt="image" src="https://github.com/user-attachments/assets/d04ab2b2-c18a-458f-b9d9-347f9bc2570c" />

echo $?
## OUTPUT 
<img width="370" height="72" alt="image" src="https://github.com/user-attachments/assets/0d009e86-5524-47b8-b11c-6599b343b14f" />
./one
bash: ./one: Permission denied

echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT

<img width="457" height="72" alt="image" src="https://github.com/user-attachments/assets/03c9f9e3-6237-4390-a5a0-ae81b1716297" />


 
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

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="520" height="285" alt="image" src="https://github.com/user-attachments/assets/a245bdeb-c00a-4f8b-81bd-d10477c161b6" />

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
<img width="542" height="77" alt="image" src="https://github.com/user-attachments/assets/868da566-e6f7-4019-934d-2dba78fb5969" />

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
<img width="670" height="475" alt="image" src="https://github.com/user-attachments/assets/3b9fd413-e0d5-471a-b4c8-7cceed56f1e7" />



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
<img width="650" height="177" alt="image" src="https://github.com/user-attachments/assets/a01e0520-2841-4f8b-920e-9a73695b2d6c" />

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
<img width="606" height="197" alt="image" src="https://github.com/user-attachments/assets/0a939e4a-3918-43ed-b743-f50c68c32731" />

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

<img width="765" height="587" alt="image" src="https://github.com/user-attachments/assets/1cc47d88-afc7-46c7-bd00-af8867979de8" />


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
<img width="707" height="256" alt="image" src="https://github.com/user-attachments/assets/df9b56c8-f705-412c-a704-5e51e21150b0" />


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
## OUTPUT
<img width="412" height="56" alt="image" src="https://github.com/user-attachments/assets/a945d634-6865-40bf-8a64-858ad2c6b3e6" />

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
## OUTPUT

<img width="402" height="332" alt="image" src="https://github.com/user-attachments/assets/e4940b45-f57c-4403-855b-6e6e92395627" />

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
 
## OUTPUT
 <img width="647" height="186" alt="image" src="https://github.com/user-attachments/assets/ddf667ed-152a-4891-ab5a-a4f7a7c4189a" />

 
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
 
## OUTPUT
<img width="722" height="271" alt="image" src="https://github.com/user-attachments/assets/abf9c60e-cb27-44be-b4f0-28883ea5d154" />

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
## OUTPUT

<img width="782" height="180" alt="image" src="https://github.com/user-attachments/assets/fa261895-50b1-46f2-939f-f0c221605d2e" />

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
## OUTPUT

<img width="895" height="272" alt="image" src="https://github.com/user-attachments/assets/440da63e-264b-4d29-a2b3-4cb6d476fce2" />

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

<img width="396" height="181" alt="image" src="https://github.com/user-attachments/assets/80d2cbed-ffd6-4607-b31e-22af45f6c0e1" />

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

<img width="356" height="180" alt="image" src="https://github.com/user-attachments/assets/8b0479d2-27c2-4532-b014-ee56fee5cb17" />

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

<img width="422" height="181" alt="image" src="https://github.com/user-attachments/assets/443e2c9f-2630-493d-ac63-c7249e50784a" />

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

<img width="351" height="401" alt="image" src="https://github.com/user-attachments/assets/2e94dd10-ee2e-4faf-bc34-07c6ec2c9338" />

 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

 <img width="325" height="80" alt="image" src="https://github.com/user-attachments/assets/c446f0b1-af33-414d-9a6f-dc230f424bb4" />

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

 <img width="376" height="190" alt="image" src="https://github.com/user-attachments/assets/c89877a6-e848-48c0-87f2-9a46cb366b98" />

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

<img width="451" height="92" alt="image" src="https://github.com/user-attachments/assets/3a8f2c50-af9b-4768-a71b-e6cfd8a4a028" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="470" height="100" alt="image" src="https://github.com/user-attachments/assets/043fac76-b96c-4979-b431-6ff87cc442a0" />



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

<img width="400" height="61" alt="image" src="https://github.com/user-attachments/assets/74f897de-7b77-4b42-b6a3-86be47b3ed6c" />

 
 ./funcex.sh 1 2


 <img width="301" height="62" alt="image" src="https://github.com/user-attachments/assets/2391c4e7-4224-40e3-a649-7af7e756ae64" />

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
 <img width="387" height="115" alt="image" src="https://github.com/user-attachments/assets/04007cf8-05e1-499b-b086-0bbddbb1dfa0" />

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
 <img width="340" height="125" alt="image" src="https://github.com/user-attachments/assets/bdda31a4-a685-4083-99be-091dff91b8dd" />

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
 <img width="595" height="487" alt="image" src="https://github.com/user-attachments/assets/f7aade0f-b961-44d0-b6b1-16c53164168e" />

 
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
 <img width="521" height="450" alt="image" src="https://github.com/user-attachments/assets/79cd3c13-f740-4d7e-a6ea-b6151558f82e" />

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

<img width="661" height="686" alt="image" src="https://github.com/user-attachments/assets/ca5fa2c7-4305-44ef-a4e4-e7bfcd23b749" />

# RESULT:
The Commands are executed successfully.

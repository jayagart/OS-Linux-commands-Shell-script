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
<img width="289" height="152" alt="image" src="https://github.com/user-attachments/assets/2ebb080b-35a9-4a5f-95cc-17f1f1fb187e" />



cat < file2

## OUTPUT

<img width="271" height="150" alt="image" src="https://github.com/user-attachments/assets/5d666fd0-394b-4ab4-95cc-5625fba5803a" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="364" height="72" alt="image" src="https://github.com/user-attachments/assets/779c1d9e-f146-4c7f-8d27-155a49021375" />

comm file1 file2
 ## OUTPUT
<img width="297" height="200" alt="image" src="https://github.com/user-attachments/assets/3b7e5701-9ccc-4e76-82d9-f0e8c2ef0cb3" />

 
diff file1 file2
## OUTPUT
<img width="274" height="279" alt="image" src="https://github.com/user-attachments/assets/ba40a2b6-3c0e-453b-8df9-6670955fa7e2" />


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

<img width="236" height="80" alt="image" src="https://github.com/user-attachments/assets/47afe5da-55de-4630-b00f-c397c38f8911" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="313" height="131" alt="image" src="https://github.com/user-attachments/assets/caa9fbe5-704f-41ae-87b2-1f8375156a1c" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="315" height="130" alt="image" src="https://github.com/user-attachments/assets/184bd34c-b57b-4c32-bb2b-44ab9425dbe7" />


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
<img width="304" height="82" alt="image" src="https://github.com/user-attachments/assets/ae06682e-dc10-4ad0-8725-f7d96b9267ca" />



grep hello newfile 
## OUTPUT
 <img width="328" height="78" alt="image" src="https://github.com/user-attachments/assets/14ebbc86-a4ef-4b00-9b08-525517678ecb" />




grep -v hello newfile 
## OUTPUT
<img width="305" height="79" alt="image" src="https://github.com/user-attachments/assets/f336ea69-789a-4702-9570-a7be7b4035ff" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="394" height="107" alt="image" src="https://github.com/user-attachments/assets/2f61ec25-e6b1-4bd5-97fc-e860467aa404" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="411" height="78" alt="image" src="https://github.com/user-attachments/assets/0cafd923-5a30-4f25-8a9c-00ae4c92e11d" />




grep -R ubuntu /etc
## OUTPUT
<img width="811" height="590" alt="image" src="https://github.com/user-attachments/assets/c932ec6c-ff50-4ef2-9019-6d1c4816aeae" />



grep -w -n world newfile   
## OUTPUT
<img width="342" height="101" alt="image" src="https://github.com/user-attachments/assets/e368bf27-5644-4898-97dc-f46a6a9895c3" />


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
<img width="400" height="100" alt="image" src="https://github.com/user-attachments/assets/9274852b-55a4-4265-9483-ab0509f33e0c" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="359" height="109" alt="image" src="https://github.com/user-attachments/assets/6c5b7a12-64be-409e-8205-9e772d3a2abc" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="405" height="101" alt="image" src="https://github.com/user-attachments/assets/a019d4eb-ce2d-42f4-b69d-5a5895623825" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="321" height="85" alt="image" src="https://github.com/user-attachments/assets/ddbae40f-439f-4c3f-8065-4afcd7d172ba" />



egrep '(world$)' newfile 
## OUTPUT
<img width="338" height="106" alt="image" src="https://github.com/user-attachments/assets/6899bbf0-c8e6-4948-bfe4-27146c0899e5" />



egrep '(World$)' newfile 
## OUTPUT
<img width="336" height="81" alt="image" src="https://github.com/user-attachments/assets/569d00df-a8e7-4592-aa46-8fbaebf641d1" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="357" height="127" alt="image" src="https://github.com/user-attachments/assets/63a2c542-680b-4980-9d74-9c51bdbda9ba" />




egrep '[1-9]' newfile 
## OUTPUT
<img width="297" height="80" alt="image" src="https://github.com/user-attachments/assets/1d8b9b82-30a9-4771-9da3-559911a208e8" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="362" height="87" alt="image" src="https://github.com/user-attachments/assets/3dedef5c-662f-4848-8198-34511e2ac94e" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="360" height="78" alt="image" src="https://github.com/user-attachments/assets/22c40349-6b67-4caa-aeb7-3395525bda8f" />


egrep l{2} newfile
## OUTPUT
<img width="295" height="103" alt="image" src="https://github.com/user-attachments/assets/2baf8c5e-54fa-4282-af50-69a500eecde8" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="369" height="132" alt="image" src="https://github.com/user-attachments/assets/b3710e8c-6a5d-4587-80f5-776d10f5b0c3" />


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
<img width="302" height="83" alt="image" src="https://github.com/user-attachments/assets/158b68a6-e5e3-4296-969a-b74432d404ff" />



sed -n -e '$p' file23
## OUTPUT
<img width="294" height="80" alt="image" src="https://github.com/user-attachments/assets/20e20a80-6e91-4218-b976-ab03f072a5ab" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="378" height="252" alt="image" src="https://github.com/user-attachments/assets/14d7bc5d-f27d-4e27-981f-d6e9eecbfa6a" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="407" height="249" alt="image" src="https://github.com/user-attachments/assets/e335dbc4-887b-4417-a212-fa4d0ceda6dd" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="391" height="248" alt="image" src="https://github.com/user-attachments/assets/0dadfc7f-a054-4755-879f-f2a00ce49b8c" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="337" height="174" alt="image" src="https://github.com/user-attachments/assets/572be924-ba2c-408b-a8a6-8ed506284b2c" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="364" height="129" alt="image" src="https://github.com/user-attachments/assets/6d86c75e-bbb5-46a2-a673-ecd7d2cb0a3f" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="391" height="108" alt="image" src="https://github.com/user-attachments/assets/c669b629-36bf-41d1-b252-bb80ee4a3456" />



seq 10 
## OUTPUT
<img width="362" height="310" alt="image" src="https://github.com/user-attachments/assets/eed6f4df-6a75-4fb7-8432-7547542db15f" />




seq 10 | sed -n '4,6p'
## OUTPUT
<img width="298" height="127" alt="image" src="https://github.com/user-attachments/assets/d2fd639b-f43d-4710-bfa1-ea548228cbff" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="330" height="123" alt="image" src="https://github.com/user-attachments/assets/efddd1c2-54b8-4223-9ea4-bc2e29b8e0e6" />




seq 3 | sed '2a hello'
## OUTPUT
<img width="298" height="153" alt="image" src="https://github.com/user-attachments/assets/ef8c05c2-f82b-437b-8d96-92fb51104e8b" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="300" height="128" alt="image" src="https://github.com/user-attachments/assets/182d5f4b-0c93-4ca2-90bb-ea9fc69d06bf" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="339" height="127" alt="image" src="https://github.com/user-attachments/assets/6e3486bd-3f16-4427-bc56-eb88debac134" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="408" height="123" alt="image" src="https://github.com/user-attachments/assets/067ee2d6-5b5b-4b5d-8ecf-fe522f3b2ba7" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="402" height="126" alt="image" src="https://github.com/user-attachments/assets/5a2dd727-0323-44ff-9bb2-b2aa7c72d434" />


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
<img width="370" height="176" alt="image" src="https://github.com/user-attachments/assets/e4398626-76cf-41ef-b93c-63f8b9e19c4c" />


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
<img width="388" height="174" alt="image" src="https://github.com/user-attachments/assets/edcdcde6-c986-4452-8841-c69cfe728911" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="440" height="257" alt="image" src="https://github.com/user-attachments/assets/d1063fef-46f7-428f-87be-8a8a7949ee36" />

cat > urllist.txt
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
<img width="387" height="122" alt="image" src="https://github.com/user-attachments/assets/2f86d924-feae-47cd-b8ab-f33b9ba2424f" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="486" height="132" alt="image" src="https://github.com/user-attachments/assets/5ed42d21-e853-4740-812e-8ce3d2b12cb1" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="357" height="576" alt="image" src="https://github.com/user-attachments/assets/4e1d1fc1-e33a-4ce2-805e-d67ea06061c7" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="766" height="600" alt="image" src="https://github.com/user-attachments/assets/decf252a-c3d5-4fdc-a65b-e47504622a4a" />


tar -xvf backup.tar
## OUTPUT
<img width="500" height="579" alt="image" src="https://github.com/user-attachments/assets/fd3a6516-1f92-48aa-8f83-0c99472220a3" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="353" height="106" alt="image" src="https://github.com/user-attachments/assets/2864f95d-40bc-4461-b555-18e9577a440e" />

gunzip backup.tar.gz
## OUTPUT
<img width="380" height="51" alt="image" src="https://github.com/user-attachments/assets/a7120f5f-e957-4b6e-9809-4a4b322ee794" />

 

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="308" height="124" alt="image" src="https://github.com/user-attachments/assets/f20cc3ad-b9c0-41b5-b8ab-cc334a108375" />


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
<img width="628" height="426" alt="image" src="https://github.com/user-attachments/assets/4a9d6cd5-1a86-4520-abf5-6a92c55e0e50" />

 
ls file1
## OUTPUT
<img width="287" height="69" alt="image" src="https://github.com/user-attachments/assets/580a51f8-f3ca-4a15-acfb-ddb832f4e985" />

echo $?
## OUTPUT 
<img width="280" height="78" alt="image" src="https://github.com/user-attachments/assets/b84c3d99-6279-4fa1-9677-7e0ab9e7a878" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="319" height="75" alt="image" src="https://github.com/user-attachments/assets/9e2bd4d5-70cf-40ce-bbc6-0879ce7cff18" />

abcd
 
echo $?
 ## OUTPUT
<img width="295" height="77" alt="image" src="https://github.com/user-attachments/assets/b209b4e4-156c-4a5d-baef-dab8f08ae05e" />


 
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
<img width="401" height="300" alt="image" src="https://github.com/user-attachments/assets/58dec5e9-802b-45e9-a246-82dc38702bcb" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="401" height="300" alt="image" src="https://github.com/user-attachments/assets/073ca699-1eb7-4add-9f04-90c2d70d2d19" />


# check file ownership
cat > psswdperm.sh 
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
<img width="665" height="253" alt="image" src="https://github.com/user-attachments/assets/347e5fab-edbc-4772-9bdb-eec68b9e4335" />

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
<img width="483" height="501" alt="image" src="https://github.com/user-attachments/assets/7c6729a3-2b90-4001-b5ab-c732baafb090" />



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
<img width="540" height="397" alt="image" src="https://github.com/user-attachments/assets/d909b6db-1742-4413-85c2-e00316151209" />

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
fchmodi
```

$ chmod 755 ifnested.sh
 
$ ./ifnested.sh 
##OUTPUT
<img width="572" height="506" alt="image" src="https://github.com/user-attachments/assets/568b7cfb-04ad-4132-a9b0-dd85cc6f042a" />


# looking for a possible value using elif
cat > elifcheck.sh 
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
<img width="615" height="503" alt="image" src="https://github.com/user-attachments/assets/c7deeef1-6192-4ae3-847a-e7c86080100c" />


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
<img width="549" height="251" alt="image" src="https://github.com/user-attachments/assets/fe768868-31a6-454b-80a8-697d96e34f4b" />

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
 <img width="619" height="320" alt="image" src="https://github.com/user-attachments/assets/95e9d6b5-2906-4bd5-bb2f-362400724f95" />

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
 <img width="451" height="246" alt="image" src="https://github.com/user-attachments/assets/e1b10186-ce51-46ce-8b53-46b96db3a5ad" />

 
cat >untiltest.sh 
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
 <img width="490" height="401" alt="image" src="https://github.com/user-attachments/assets/e02b551a-54bf-4523-8d92-18debedfbde5" />

 
 
cat >forin1.sh 
```bash
\#!/bin/bash
\#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
 <img width="612" height="258" alt="image" src="https://github.com/user-attachments/assets/c2ba3a7e-42d3-4897-b035-1b9deb16deee" />

 
cat >forin2.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
cat >forin2.sh 
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
<img width="616" height="181" alt="image" src="https://github.com/user-attachments/assets/7cea0faa-70ce-4a56-879e-ef1d67fe6bd7" />
 
cat >forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ ./forin3.sh 
<img width="354" height="252" alt="image" src="https://github.com/user-attachments/assets/eead574e-548f-4653-8d64-44e31bbb1135" />
 
cat >forin1.sh 
```bash
#!/bin/bash
# basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
```
$ chmod 755 forin1.sh
<img width="377" height="256" alt="image" src="https://github.com/user-attachments/assets/0377499c-732a-4b02-9bc1-d61de61e9363" />

## OUTPUT
cat >forinfile.sh 
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
<img width="681" height="504" alt="image" src="https://github.com/user-attachments/assets/6b05d51d-d7e1-4f62-9dc4-2543d126b186" />


cat > forctype.sh 
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
<img width="323" height="231" alt="image" src="https://github.com/user-attachments/assets/f766a35a-fab0-4b7d-a4d1-27e9f566a6cb" />

cat >forctype1.sh 
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
<img width="287" height="171" alt="image" src="https://github.com/user-attachments/assets/4bfb620f-8835-4e0c-a0a6-27bfe6fb5036" />

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
<img width="332" height="550" alt="image" src="https://github.com/user-attachments/assets/e22b00ae-2ce9-434b-aa43-8f28a343ced8" />

 
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
 <img width="344" height="149" alt="image" src="https://github.com/user-attachments/assets/d88beead-09f5-432b-ae49-f8abfe9afae1" />

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
<img width="350" height="197" alt="image" src="https://github.com/user-attachments/assets/81d8ca48-c373-4eb2-a037-a4ab7ab1f8a4" />
 
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
<img width="482" height="296" alt="image" src="https://github.com/user-attachments/assets/0023817f-edcf-4827-9f33-b6263bc51277" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="506" height="273" alt="image" src="https://github.com/user-attachments/assets/c9de848d-3567-4d44-a5c0-8d4a919e2f3b" />



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
<img width="608" height="375" alt="image" src="https://github.com/user-attachments/assets/9d72829e-f74f-4acb-a85a-0c0d76205ff2" />

 
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
<img width="395" height="196" alt="image" src="https://github.com/user-attachments/assets/8df39112-bbea-40f3-a610-875c9e4d632e" />

$ ./argshift.sh 1 2 3
 
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
 <img width="597" height="475" alt="image" src="https://github.com/user-attachments/assets/1fd60c3c-744b-4d7c-afec-2f7070171adb" />

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
 <img width="408" height="453" alt="image" src="https://github.com/user-attachments/assets/89e2cd0f-7b61-45fc-8ef2-cfcc07336387" />

 
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
awk
awk -f nc.awk data.dat
## OUTPUT 
 <img width="418" height="381" alt="image" src="https://github.com/user-attachments/assets/37678295-df8e-40a3-ab3e-aff4d80b4f91" />

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
<img width="452" height="256" alt="image" src="https://github.com/user-attachments/assets/c3504d28-1762-4305-a12b-20d4724b4a34" />


# RESULT:
The Commands are executed successfully.

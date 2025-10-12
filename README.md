# OS-Linux-commands-Shell-scripting
Operating systems Lab exercise
# Linux commands-Shell scripting
Linux commands-Shell scripting

# AIM:
12/10/2025
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
![Alt text](../../1.png)


cat < file2

## OUTPUT
![Alt text](../../2.png)


# Comparing Files
cmp file1 file2
## OUTPUT
![Alt text](../../3.png)

comm file1 file2
 ## OUTPUT
![Alt text](../../4.png)
 
diff file1 file2
## OUTPUT
![Alt text](../../5.png)


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
![Alt text](../../6.png)

cut -d "|" -f 1 file22
## OUTPUT
![Alt text](../../7.png)



cut -d "|" -f 2 file22
## OUTPUT
![Alt text](../../8.png)

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
![Alt text](../../9.png)



grep -v hello newfile 
## OUTPUT
![Alt text](../../10.png)



cat newfile | grep -i "hello"
## OUTPUT
![Alt text](../../11.png)



cat newfile | grep -i -c "hello"
## OUTPUT
![Alt text](../../12.png)




grep -R ubuntu /etc
## OUTPUT
![Alt text](../../13.png)



grep -w -n world newfile   
![Alt text](../../14.png)## OUTPUT



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
![Alt text](../../15.png)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Alt text](../../16.png)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT



egrep '(^hello)' newfile 
## OUTPUT
![Alt text](../../17.png)



egrep '(world$)' newfile 
## OUTPUT
![Alt text](../../18.png)



egrep '(World$)' newfile 
## OUTPUT
![Alt text](../../19.png)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Alt text](image-1.png)


egrep '[1-9]' newfile 
## OUTPUT
![Alt text](image-2.png)


egrep 'Linux.*world' newfile 
## OUTPUT
![Alt text](image-3.png)


egrep 'Linux.*World' newfile 
## OUTPUT
![Alt text](../../26.png)


egrep l{2} newfile
## OUTPUT
![Alt text](../../27.png)



egrep 's{1,2}' newfile
## OUTPUT 
![Alt text](../../28.png)


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
![Alt text](../../29.png)


sed -n -e '$p' file23
## OUTPUT
![Alt text](../../30.png)



sed  -e 's/Ram/Sita/' file23
## OUTPUT

![Alt text](../../31.png)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Alt text](../../32.png)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Alt text](../../33.png)


sed -n -e '1,5p' file23
## OUTPUT
![Alt text](../../34.png)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Alt text](../../35.png)

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Alt text](../../36.png)



seq 10 
## OUTPUT
![Alt text](../../37.png)


seq 10 | sed -n '4,6p'
## OUTPUT
<
![Alt text](../../38.png)

seq 10 | sed -n '2,~4p'
## OUTPUT
![Alt text](../../39.png)


seq 3 | sed '2a hello'
## OUTPUT
![Alt text](../../40.png)



seq 2 | sed '2i hello'
## OUTPUT
![Alt text](../../41.png)


seq 10 | sed '2,9c hello'
## OUTPUT
![Alt text](../../42.png)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Alt text](../../43.png)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
![Alt text](../../44.png)


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
![Alt text](../../45.png)


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
<img width="663" height="176" alt="image" src="https://github.com/user-attachments/assets/62ad75df-0b8d-407a-9a46-b4d31e91119b" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="624" height="251" alt="image" src="https://github.com/user-attachments/assets/ebeedf4e-7552-40a4-86f2-d7c9ac6c98e0" />

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
<img width="665" height="126" alt="image" src="https://github.com/user-attachments/assets/7f29b970-9da4-43c0-bee6-9fa9b75f8c6d" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="645" height="118" alt="image" src="https://github.com/user-attachments/assets/5cbf4546-c06f-4608-8e13-bc3010f6b8b1" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="663" height="350" alt="image" src="https://github.com/user-attachments/assets/8fbcfe51-a7a7-422e-b326-4233c33d929b" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="729" height="364" alt="image" src="https://github.com/user-attachments/assets/7db77142-ab5d-4771-b5d4-f7cbb535ea66" />


tar -xvf backup.tar
## OUTPUT
<img width="740" height="347" alt="image" src="https://github.com/user-attachments/assets/1831e825-9b55-4e5e-9e8d-ef7397c6ce06" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="754" height="152" alt="image" src="https://github.com/user-attachments/assets/8aa6a736-0107-41c0-b5bb-a1b3bcf1257a" />


cat > scriptest.sh 
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

cat >scriptest.sh 
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
<img width="777" height="353" alt="image" src="https://github.com/user-attachments/assets/253970a0-1a65-4541-8e9b-04b6d694c7f2" />

 
ls file1
## OUTPUT
<img width="733" height="75" alt="image" src="https://github.com/user-attachments/assets/a0932a6f-f578-4636-862e-430578cdd0c2" />

echo $?
## OUTPUT 
<img width="724" height="70" alt="image" src="https://github.com/user-attachments/assets/86eb8e94-756a-4919-bae7-c173b17b8b88" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="724" height="70" alt="image" src="https://github.com/user-attachments/assets/86eb8e94-756a-4919-bae7-c173b17b8b88" />

abcd
 
echo $?
 ## OUTPUT
<img width="724" height="70" alt="image" src="https://github.com/user-attachments/assets/86eb8e94-756a-4919-bae7-c173b17b8b88" />


 
# mis-using string comparisons

cat > strcomp.sh 
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
<img width="794" height="128" alt="image" src="https://github.com/user-attachments/assets/7999d30c-2580-44e3-b4cf-de1dd22b2947" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="794" height="128" alt="image" src="https://github.com/user-attachments/assets/7999d30c-2580-44e3-b4cf-de1dd22b2947" />


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
<img width="738" height="82" alt="image" src="https://github.com/user-attachments/assets/1e4ba9ca-3bcb-4b8a-bf97-575ebe303c47" />

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

<img width="640" height="126" alt="image" src="https://github.com/user-attachments/assets/8c2e9c15-a581-41da-80b5-1fe0e2b55229" />


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
```

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
##OUTPUT
<img width="635" height="103" alt="image" src="https://github.com/user-attachments/assets/a2017c47-6bb0-4dfa-958c-1d55a3d594fe" />

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
<img width="672" height="178" alt="image" src="https://github.com/user-attachments/assets/08b5ada7-6228-4158-85bb-a20714319a86" />


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
<img width="674" height="129" alt="image" src="https://github.com/user-attachments/assets/78932b2f-c42e-4b63-9e4a-727259ddb3e0" />


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
<img width="686" height="125" alt="image" src="https://github.com/user-attachments/assets/828e8104-92ba-4450-8510-3df86141a630" />

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
<img width="730" height="128" alt="image" src="https://github.com/user-attachments/assets/8d38e056-356a-470c-9a58-b1a802fb79ac" />


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
<img width="712" height="353" alt="image" src="https://github.com/user-attachments/assets/bb2c3bfc-9f8c-496c-a956-1f3fed5893cb" />

 
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
<img width="686" height="225" alt="image" src="https://github.com/user-attachments/assets/ee4ec23d-c266-4258-bfed-c52814c4b0aa" />

 
 
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
<img width="691" height="276" alt="image" src="https://github.com/user-attachments/assets/57952930-6313-4795-a6d0-2f7f8c1a99c4" />

 
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
 <img width="693" height="195" alt="image" src="https://github.com/user-attachments/assets/ecaa0290-452f-42fb-abdc-b542d4818088" />

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
<img width="693" height="195" alt="image" src="https://github.com/user-attachments/assets/bae1c1f4-e746-4fda-b848-4f92a8f45336" />
 
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
 <img width="721" height="279" alt="image" src="https://github.com/user-attachments/assets/616a0ab5-9b14-4c16-9247-675c370059f9" />

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

##<img width="696" height="251" alt="image" src="https://github.com/user-attachments/assets/425f763c-44f9-4583-b0e2-96aafd392542" />
 OUTPUT

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
<img width="683" height="229" alt="image" src="https://github.com/user-attachments/assets/55bee3f7-bf01-40d8-b5b7-1e399090ee95" />


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
<img width="620" height="179" alt="image" src="https://github.com/user-attachments/assets/68e21ec6-5e3a-4fad-bda7-4d277b1bfe4b" />

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
<img width="662" height="180" alt="image" src="https://github.com/user-attachments/assets/3714dcb6-25f4-410f-8c58-133420097ea6" />

cat >fornested1.sh 
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
<img width="683" height="404" alt="image" src="https://github.com/user-attachments/assets/d15973f8-57a6-4c30-a0b2-46d2d6919aa4" />

 
cat > forbreak.sh 
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
<img width="734" height="127" alt="image" src="https://github.com/user-attachments/assets/9bec9a74-7a4d-448c-929d-eae34e64e0e4" />

cat > forbreak.sh 
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
 <img width="734" height="127" alt="image" src="https://github.com/user-attachments/assets/9bec9a74-7a4d-448c-929d-eae34e64e0e4" />

cat > exread.sh 
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
<img width="686" height="151" alt="image" src="https://github.com/user-attachments/assets/8abee8e3-0de3-41aa-bbc9-c902be638d1d" />


 cat > exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="695" height="127" alt="image" src="https://github.com/user-attachments/assets/15708642-1356-46d2-b7c3-1cd22ae6f8a5" />



$ ./exread1.sh 
 
cat > funcex.sh
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
<img width="676" height="202" alt="image" src="https://github.com/user-attachments/assets/844bdea5-aac6-4cec-8136-a2f6b19a55a8" />

 
cat > argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh

## OUTPUT
<img width="680" height="176" alt="image" src="https://github.com/user-attachments/assets/817d283d-46fd-4cf0-8719-b2d8a0df1e50" />

$ ./argshift.sh 1 2 3
 
 cat > argshift1.sh
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
<img width="689" height="173" alt="image" src="https://github.com/user-attachments/assets/9279b4f5-401f-41af-a53a-43146a54cc9a" />

cat > argshift.sh
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
<img width="673" height="452" alt="image" src="https://github.com/user-attachments/assets/116b8eda-7245-4f4f-8285-f6ba65da2361" />

 
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
<img width="705" height="376" alt="image" src="https://github.com/user-attachments/assets/ef66e90f-20c1-46f6-a1df-25428aec9b22" />

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
<img width="679" height="177" alt="image" src="https://github.com/user-attachments/assets/f8cfd156-411e-48d6-baf6-9ed18b8587a9" />


# RESULT:
The Commands are executed successfully.

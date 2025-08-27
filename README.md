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

<img width="475" height="216" alt="image" src="https://github.com/user-attachments/assets/03d130c3-9389-44f7-85d9-bd14384a7e9a" />




cat < file2
## OUTPUT

<img width="637" height="232" alt="image" src="https://github.com/user-attachments/assets/168fdbae-c2e0-4eac-84df-6fb47a78d99b" />

cmp file1 file2
## OUTPUT
<img width="597" height="100" alt="image" src="https://github.com/user-attachments/assets/941a5a6e-c257-4f20-b6ac-303d664e7bd5" />

 
comm file1 file2
 ## OUTPUT
<img width="602" height="307" alt="image" src="https://github.com/user-attachments/assets/621fb15d-52f5-42b4-8930-ec961ac944c8" />

 
diff file1 file2
## OUTPUT
<img width="483" height="382" alt="image" src="https://github.com/user-attachments/assets/d898b943-cde2-48c0-b9e4-13b6531f715e" />



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

<img width="463" height="145" alt="image" src="https://github.com/user-attachments/assets/cf3874ef-2083-41c4-9b57-a4f2c3cd5534" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="542" height="173" alt="image" src="https://github.com/user-attachments/assets/5849690d-e118-4024-bb93-eeb82f81e392" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="485" height="167" alt="image" src="https://github.com/user-attachments/assets/49df2a14-608d-4b46-b77c-b793a6fe0ca1" />

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
<img width="477" height="103" alt="image" src="https://github.com/user-attachments/assets/6eeda1eb-3be2-4108-a18c-f7ecfd2e5846" />



grep hello newfile 
## OUTPUT
<img width="516" height="102" alt="image" src="https://github.com/user-attachments/assets/63c89ce8-1b57-4de9-95f8-05ec6877c0c9" />



grep -v hello newfile 
## OUTPUT

<img width="617" height="147" alt="image" src="https://github.com/user-attachments/assets/9e13e888-5e96-41e8-979b-14ba5f593e8b" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="592" height="107" alt="image" src="https://github.com/user-attachments/assets/d0ea8e8d-bc96-4e3b-b2da-c64c9f34e19b" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="652" height="107" alt="image" src="https://github.com/user-attachments/assets/ce32e42a-e7eb-46f4-9782-0893df4a2eee" />



grep -R ubuntu /etc
## OUTPUT

<img width="957" height="517" alt="image" src="https://github.com/user-attachments/assets/1bc19ea2-9f0c-4afc-9ad7-6c718cebeb60" />

grep -w -n world newfile   
## OUTPUT
<img width="522" height="141" alt="image" src="https://github.com/user-attachments/assets/1d8d33af-6b2a-4f05-ac6d-caf11091abf6" />


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
<img width="578" height="141" alt="image" src="https://github.com/user-attachments/assets/0723af5f-1a7b-4735-a1e6-74e9f8872fe9" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="642" height="148" alt="image" src="https://github.com/user-attachments/assets/e7366a87-d0a7-4e1d-a107-e5a1781087a6" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="746" height="137" alt="image" src="https://github.com/user-attachments/assets/70f7781e-d04b-47c4-b20b-a77d85697017" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="556" height="120" alt="image" src="https://github.com/user-attachments/assets/4be2de18-7bd0-4aa4-adba-953121c8f4cc" />


egrep '(world$)' newfile 
## OUTPUT
<img width="561" height="172" alt="image" src="https://github.com/user-attachments/assets/d5e95269-ac60-44f7-838f-ff45df9c4371" />



egrep '(World$)' newfile 
## OUTPUT
<img width="541" height="112" alt="image" src="https://github.com/user-attachments/assets/39402069-6e80-43a5-8631-3fbd342b5d1e" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="568" height="138" alt="image" src="https://github.com/user-attachments/assets/f0098264-a82b-4d24-b9ac-ff33ed7e3531" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="517" height="112" alt="image" src="https://github.com/user-attachments/assets/94e3eef8-c2be-4b92-860b-b4c87828de7f" />




egrep 'Linux.*world' newfile 
## OUTPUT
<img width="531" height="146" alt="image" src="https://github.com/user-attachments/assets/a0cc4f81-4a43-4bea-9246-0255c5b7dec1" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="618" height="107" alt="image" src="https://github.com/user-attachments/assets/6444d1cc-7242-423f-9d4a-245183e42c4f" />



egrep l{2} newfile
## OUTPUT

<img width="550" height="138" alt="image" src="https://github.com/user-attachments/assets/149a8ab0-09d5-43bc-9fb5-091bd6b24904" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="540" height="177" alt="image" src="https://github.com/user-attachments/assets/5c5057a0-22bd-48de-be8f-92463e971412" />


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

<img width="511" height="115" alt="image" src="https://github.com/user-attachments/assets/0585fc70-cc5d-4193-bb9b-4b7a1ee6c372" />



sed -n -e '$p' file23
## OUTPUT

<img width="557" height="100" alt="image" src="https://github.com/user-attachments/assets/d3bf3a24-065c-49de-8a54-ca500a7b19af" />

sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="573" height="357" alt="image" src="https://github.com/user-attachments/assets/02b22973-6e6e-4755-bf67-a0dbd1ea6615" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="632" height="348" alt="image" src="https://github.com/user-attachments/assets/0d56c0b1-85ff-4f0d-927a-9769e2806401" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="607" height="351" alt="image" src="https://github.com/user-attachments/assets/ba148ae4-24a6-4e23-85c8-c4b966df666a" />

sed -n -e '1,5p' file23
## OUTPUT

<img width="540" height="252" alt="image" src="https://github.com/user-attachments/assets/7351e7bb-4d01-4f35-988d-a8f716a2d8fa" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="646" height="177" alt="image" src="https://github.com/user-attachments/assets/c0cfc704-5b55-4a84-ae2f-1fd92dc29bd1" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="696" height="137" alt="image" src="https://github.com/user-attachments/assets/76ffd7a7-7394-4b08-89fa-bb66b67ed463" />


seq 10 
## OUTPUT

<img width="550" height="417" alt="image" src="https://github.com/user-attachments/assets/524e8ea4-a761-4d54-b973-a9e7c9513013" />

seq 10 | sed -n '4,6p'
## OUTPUT

<img width="547" height="172" alt="image" src="https://github.com/user-attachments/assets/d2034c59-51f9-4a41-9087-cbbb30520925" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="527" height="178" alt="image" src="https://github.com/user-attachments/assets/0b6aecd4-f1d3-427a-8f7a-f0939ce1ad08" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="556" height="212" alt="image" src="https://github.com/user-attachments/assets/adeb31c2-4569-4e10-9a98-56a0d99d1552" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="558" height="167" alt="image" src="https://github.com/user-attachments/assets/e54120cb-c412-4701-a3d4-05ad36136c0b" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="598" height="177" alt="image" src="https://github.com/user-attachments/assets/09298377-4a40-48de-a7dc-bc6988f96d98" />


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
<img width="545" height="245" alt="image" src="https://github.com/user-attachments/assets/6c430177-375a-4ea6-bdd5-cb73a56187bf" />

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
<img width="572" height="241" alt="image" src="https://github.com/user-attachments/assets/23847460-ccfa-4af0-bf10-89229e89af8c" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="732" height="345" alt="image" src="https://github.com/user-attachments/assets/e825ac35-bf0d-411b-bd3f-50d44b9262ad" />

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
<img width="572" height="180" alt="image" src="https://github.com/user-attachments/assets/c8abafed-bb3f-4f4e-9535-3e7a2a828069" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="866" height="201" alt="image" src="https://github.com/user-attachments/assets/45555999-15eb-4f02-87d9-9e9fb552edd5" />

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
## OUTPUT
<img width="653" height="448" alt="image" src="https://github.com/user-attachments/assets/0d0798fd-8a5e-47aa-84f6-487537dd16c6" />

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
echo 'The $\# is ' $\#
echo 'The $$ is ' $$
ps
```

 
ls file1
## OUTPUT
<img width="647" height="100" alt="image" src="https://github.com/user-attachments/assets/b530aea8-8458-47e3-8bb0-8800c2b5a6c5" />


echo $?
## OUTPUT 
<img width="518" height="110" alt="image" src="https://github.com/user-attachments/assets/0565f739-ab8b-4559-b1ff-0e0ef25f7703" />


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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT


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
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT



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


# RESULT:
The Commands are executed successfully.

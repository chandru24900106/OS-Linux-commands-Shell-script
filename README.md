## NAME : CHANDRU V
## REG NO : 212224230043
## EX : 1
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

#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="717" height="468" alt="Screenshot 2025-08-25 203609" src="https://github.com/user-attachments/assets/933986db-e02c-4611-87f7-2a6952b99b81" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="950" height="479" alt="Screenshot 2025-08-25 203647" src="https://github.com/user-attachments/assets/3aa43386-985c-48f1-9b23-c9958f478ba2" />


tar -xvf backup.tar
## OUTPUT
<img width="681" height="340" alt="Screenshot 2025-08-25 203704" src="https://github.com/user-attachments/assets/0f9080d9-6176-4443-8b15-ab0e8fd4bd00" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="718" height="134" alt="Screenshot 2025-08-25 203842" src="https://github.com/user-attachments/assets/f42207ef-dcc2-4bcb-9365-3b59b2a21a65" />



 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="873" height="481" alt="Screenshot 2025-08-26 112200" src="https://github.com/user-attachments/assets/b455dad9-0e67-4a09-b285-5eb057bf43f2" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="760" height="471" alt="Screenshot 2025-08-26 112247" src="https://github.com/user-attachments/assets/454c1844-5264-442c-8a00-48cee565dfdb" />


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
<img width="924" height="662" alt="Screenshot 2025-08-26 113447" src="https://github.com/user-attachments/assets/d0e16d73-5cc1-4fae-8dfb-7fd84ce57a7b" />

 
ls file1
## OUTPUT
<img width="503" height="113" alt="Screenshot 2025-08-26 113548" src="https://github.com/user-attachments/assets/3eda1b24-5583-48cb-9099-019d35433d29" />

echo $?
## OUTPUT 
<img width="447" height="115" alt="Screenshot 2025-08-26 113604" src="https://github.com/user-attachments/assets/c6972242-c4c1-4662-8a8f-d8b2d12f8567" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="499" height="113" alt="Screenshot 2025-08-26 113713" src="https://github.com/user-attachments/assets/f6de62f6-fe77-4fdf-a0be-151c4004ebf8" />

 
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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="923" height="241" alt="Screenshot 2025-08-26 114112" src="https://github.com/user-attachments/assets/24292b4d-d1e9-4ce0-b997-4b367f30125f" />


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

cat< psswdperm.sh 
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
<img width="885" height="345" alt="Screenshot 2025-08-26 114303" src="https://github.com/user-attachments/assets/29dcfedc-c44e-4ddb-a8aa-48b302b9ed33" />

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

<img width="955" height="365" alt="Screenshot 2025-08-26 133213" src="https://github.com/user-attachments/assets/8c6cdd27-63db-417c-8cc0-dd44368e68cd" />


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
<img width="961" height="433" alt="Screenshot 2025-08-26 133519" src="https://github.com/user-attachments/assets/64950a4e-c24b-4433-b9f8-e6b66e6f003e" />


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
<img width="537" height="114" alt="Screenshot 2025-08-31 181348" src="https://github.com/user-attachments/assets/12da0d94-95cf-4d8d-bb0a-492a00ab56d5" />

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
<img width="421" height="485" alt="Screenshot 2025-08-31 181853" src="https://github.com/user-attachments/assets/ab7e8da9-4f33-4cc9-97cc-8ed4a002ad0b" />

 
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
 
<img width="884" height="293" alt="Screenshot 2025-09-01 131533" src="https://github.com/user-attachments/assets/539da996-9243-4b17-813e-fecb3f56df55" />

 
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
 <img width="590" height="347" alt="Screenshot 2025-09-01 131651" src="https://github.com/user-attachments/assets/ce9e2d9a-9677-41cd-9e33-be2844e34631" />

 
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
<img width="596" height="208" alt="Screenshot 2025-09-01 131758" src="https://github.com/user-attachments/assets/7e6404a9-6c3e-44b9-8374-55294dfcea9d" />

cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
./forin3.sh 
<img width="511" height="344" alt="Screenshot 2025-09-01 131850" src="https://github.com/user-attachments/assets/ccf1c570-b5a3-47a2-ba1a-5cc090a3989c" />



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
<img width="527" height="217" alt="Screenshot 2025-09-01 132239" src="https://github.com/user-attachments/assets/1be94229-4776-4860-a3e7-b8c1f82b3b87" />


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
<img width="588" height="297" alt="Screenshot 2025-09-01 132327" src="https://github.com/user-attachments/assets/16a4dced-2abb-461f-b415-6a1005aa3dd6" />

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
<img width="527" height="303" alt="Screenshot 2025-09-01 132448" src="https://github.com/user-attachments/assets/f757f4aa-c551-44cf-ac7c-a9ff0b8d9acf" />


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
<img width="498" height="602" alt="Screenshot 2025-09-01 132559" src="https://github.com/user-attachments/assets/5987326b-7fa7-41ac-9ec3-9032af1f973d" />

 
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

<img width="572" height="214" alt="Screenshot 2025-09-01 132749" src="https://github.com/user-attachments/assets/9a038bbb-e414-48d6-a449-2e4cb50437d5" />

 
 

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
<img width="818" height="178" alt="Screenshot 2025-09-01 132929" src="https://github.com/user-attachments/assets/562a20b4-f45f-48a6-911c-b801caa0da58" />


 
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

 <img width="493" height="126" alt="Screenshot 2025-09-01 133225" src="https://github.com/user-attachments/assets/ec9784b8-2efe-4608-874f-7632dea8d268" />



 
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
 <img width="520" height="215" alt="Screenshot 2025-09-01 133414" src="https://github.com/user-attachments/assets/27b2d9e7-d0a7-4005-a0e0-3bda6f74bbbd" />

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
<img width="519" height="215" alt="Screenshot 2025-09-01 133526" src="https://github.com/user-attachments/assets/49d0deae-fc30-4f5d-ade2-92d0b0b90984" />


 
 
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
 <img width="581" height="635" alt="Screenshot 2025-09-01 133751" src="https://github.com/user-attachments/assets/df527873-b292-4b9d-838a-3ffbd7940c27" />

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
<img width="689" height="216" alt="Screenshot 2025-09-01 133907" src="https://github.com/user-attachments/assets/34766ad2-ee8a-499f-aa88-7b30ca7f73bf" />


# RESULT:
The Commands are executed successfully.

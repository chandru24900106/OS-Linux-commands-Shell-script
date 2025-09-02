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

<img width="476" height="182" alt="image" src="https://github.com/user-attachments/assets/28341669-3620-460b-9327-957e30b66371" />





cat < file2
## OUTPUT

<img width="437" height="217" alt="image" src="https://github.com/user-attachments/assets/221fe468-2ff9-4d9e-8da6-f522c06139be" />

cmp file1 file2
## OUTPUT
<img width="487" height="103" alt="image" src="https://github.com/user-attachments/assets/2d47d8de-d17f-4400-b7d6-22ef55223e85" />


 
comm file1 file2
 ## OUTPUT
<img width="493" height="277" alt="image" src="https://github.com/user-attachments/assets/d0f6efed-8547-4051-9d71-45170f90b2f4" />


 
diff file1 file2
## OUTPUT
<img width="477" height="338" alt="image" src="https://github.com/user-attachments/assets/174ff0cf-725d-4494-a122-1375e0b25bf6" />




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

<img width="487" height="122" alt="image" src="https://github.com/user-attachments/assets/7317950e-34c5-4d4d-9e06-bebbb56dbb05" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="443" height="152" alt="image" src="https://github.com/user-attachments/assets/4e3e13ed-38ea-47c0-83de-1b6d7f3b2377" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="438" height="157" alt="image" src="https://github.com/user-attachments/assets/2aab262c-de0a-4842-b98e-7419d384e910" />


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
<img width="408" height="96" alt="image" src="https://github.com/user-attachments/assets/013d1da0-0f66-4f9e-86bd-8ab71f9c3283" />




grep hello newfile 
## OUTPUT
<img width="447" height="102" alt="image" src="https://github.com/user-attachments/assets/52ce9ac5-cac0-4b0e-b1e9-724baa6cb6cf" />



grep -v hello newfile 
## OUTPUT

<img width="422" height="88" alt="image" src="https://github.com/user-attachments/assets/a5603da2-33c5-4ea0-8234-49d6dcad6472" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="485" height="127" alt="image" src="https://github.com/user-attachments/assets/6deb8cc5-cb42-443c-baec-81947f26c779" />




cat newfile | grep -i -c "hello"
## OUTPUT

<img width="486" height="93" alt="image" src="https://github.com/user-attachments/assets/cc90991b-b952-489c-8888-6c6973c9bef3" />




grep -R ubuntu /etc
## OUTPUT

<img width="483" height="335" alt="image" src="https://github.com/user-attachments/assets/366012ba-1f67-4630-bbf9-5edc623486a1" />


grep -w -n world newfile   
## OUTPUT
<img width="472" height="127" alt="image" src="https://github.com/user-attachments/assets/23aa0e63-c719-4121-b5f3-813feb8fe5f4" />



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
<img width="522" height="125" alt="image" src="https://github.com/user-attachments/assets/ca102fed-da13-4998-bf5b-e9b444b95b9d" />




egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="453" height="132" alt="image" src="https://github.com/user-attachments/assets/50de4f4a-d5d3-42dd-9dec-98dae36f0dcd" />




egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="488" height="120" alt="image" src="https://github.com/user-attachments/assets/ce4d195e-c314-4908-a261-003858502ae5" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="435" height="92" alt="image" src="https://github.com/user-attachments/assets/eebd1622-b3ac-4505-a8f6-d2bd79aeb395" />



egrep '(world$)' newfile 
## OUTPUT
<img width="437" height="127" alt="image" src="https://github.com/user-attachments/assets/09f565a6-2dcd-49d0-b7b9-32891e57c7ce" />




egrep '(World$)' newfile 
## OUTPUT
<img width="385" height="126" alt="image" src="https://github.com/user-attachments/assets/5b143073-6c09-4ea8-b7ee-668f6bf06034" />



egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="467" height="163" alt="image" src="https://github.com/user-attachments/assets/3373121a-e678-4f37-bbcd-72197e2e8ac6" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="438" height="96" alt="image" src="https://github.com/user-attachments/assets/a20d8d07-3f0b-40cf-8882-a0c68bd5c6a7" />





egrep 'Linux.*world' newfile 
## OUTPUT
<img width="473" height="108" alt="image" src="https://github.com/user-attachments/assets/db3bb962-e5a3-4b60-b355-9480a4f739dd" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="485" height="102" alt="image" src="https://github.com/user-attachments/assets/66150b34-3536-4879-90bd-5df65f4def3b" />



egrep l{2} newfile
## OUTPUT

<img width="447" height="118" alt="image" src="https://github.com/user-attachments/assets/73efc6be-fdd2-4713-8b18-0982c7a73a85" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="407" height="162" alt="image" src="https://github.com/user-attachments/assets/718f97af-779e-44b1-a0af-3ee0d215bfbd" />



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

<img width="426" height="97" alt="image" src="https://github.com/user-attachments/assets/9bac101f-7959-437a-ace9-2a589f1ff665" />




sed -n -e '$p' file23
## OUTPUT

<img width="445" height="100" alt="image" src="https://github.com/user-attachments/assets/a1ab6b3d-df91-45d7-85b3-b7484bd373a9" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="470" height="316" alt="image" src="https://github.com/user-attachments/assets/afcf4ef8-38e5-4e43-9dcd-19162f955037" />




sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="457" height="305" alt="image" src="https://github.com/user-attachments/assets/3f24cb88-22fb-486d-b614-6075445910ba" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="498" height="297" alt="image" src="https://github.com/user-attachments/assets/4fc03dfa-560a-44b1-a40d-3579769663c4" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="431" height="218" alt="image" src="https://github.com/user-attachments/assets/11763c54-5ce2-45d2-b08c-896462bed8b5" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="451" height="176" alt="image" src="https://github.com/user-attachments/assets/2d91b819-e3b3-45da-bcb0-285f3d8d2309" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="480" height="126" alt="image" src="https://github.com/user-attachments/assets/128755d0-20cd-426c-ac4e-00b157b47e22" />



seq 10 
## OUTPUT

<img width="372" height="372" alt="image" src="https://github.com/user-attachments/assets/8213f2ee-2a43-4516-9c7e-4d1e6d50a3c4" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="412" height="161" alt="image" src="https://github.com/user-attachments/assets/9f977700-1d8d-4982-8f68-0aec66d1abda" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="427" height="157" alt="image" src="https://github.com/user-attachments/assets/f060c8c1-a713-425e-912b-9481c0884fc0" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="551" height="186" alt="image" src="https://github.com/user-attachments/assets/ce24528d-e5a4-4e28-a7e5-e2fcd8cdba29" />




seq 10 | sed '2,9c hello'
## OUTPUT
<img width="395" height="152" alt="image" src="https://github.com/user-attachments/assets/8ff0aa5a-fa09-49f0-9297-92cdbde33f57" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="482" height="152" alt="image" src="https://github.com/user-attachments/assets/9fe0dae9-c2ba-46db-ace6-5bc1ff775fd3" />



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
<img width="428" height="226" alt="image" src="https://github.com/user-attachments/assets/b9a3802f-2c23-4224-b8a8-14b6d25c80a6" />


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
<img width="420" height="217" alt="image" src="https://github.com/user-attachments/assets/51fd6c96-3dc4-40cb-9e18-10ebbf0c9145" />




#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="503" height="306" alt="image" src="https://github.com/user-attachments/assets/555ffccf-1809-4190-9077-e1688f595314" />


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
<img width="457" height="147" alt="image" src="https://github.com/user-attachments/assets/9fe05554-d401-4175-9add-b887e554fb18" />



 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="567" height="165" alt="image" src="https://github.com/user-attachments/assets/e83c9549-af3c-455b-a505-c0a0aaee4866" />


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

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
<img width="407" height="265" alt="image" src="https://github.com/user-attachments/assets/ed8fd391-f769-411f-9d86-45dccd466e68" />



mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="615" height="267" alt="image" src="https://github.com/user-attachments/assets/80596fe1-16c0-4538-9b87-fc1206d4621c" />



tar -xvf backup.tar
## OUTPUT
<img width="515" height="252" alt="image" src="https://github.com/user-attachments/assets/756cad43-8f29-4e57-a49e-79e415c8d206" />


gzip backup.tar

ls .gz
## OUTPUT
<img width="437" height="83" alt="image" src="https://github.com/user-attachments/assets/3a743946-a4f4-435e-b8ce-421b6f5f2951" />





 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="354" height="126" alt="Screenshot 2025-08-31 173253" src="https://github.com/user-attachments/assets/482567b5-c276-4f90-b655-938824738ef6" />


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
<img width="535" height="129" alt="Screenshot 2025-08-31 185331" src="https://github.com/user-attachments/assets/a2932fc9-5049-44cc-8002-83a7f7546607" />

 
ls file1
## OUTPUT
<img width="330" height="70" alt="Screenshot 2025-08-31 185402" src="https://github.com/user-attachments/assets/11fe3d0c-15ec-4240-a222-d717fca8f81b" />

echo $?
## OUTPUT 
<img width="289" height="74" alt="Screenshot 2025-08-31 185448" src="https://github.com/user-attachments/assets/67371631-9f08-45f1-95d5-cbe4b1aeba83" />

./one
bash: ./one: Permission denied
 

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

<img width="455" height="287" alt="Screenshot 2025-08-31 190313" src="https://github.com/user-attachments/assets/a941002e-697b-42cb-8838-f10fad0e6455" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="670" height="181" alt="Screenshot 2025-08-31 190413" src="https://github.com/user-attachments/assets/858f6626-351f-49e9-a441-5450de310765" />


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
<img width="642" height="303" alt="Screenshot 2025-08-31 191128" src="https://github.com/user-attachments/assets/62c464f0-410a-4786-acf4-73d5c2fae5f9" />

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

<img width="599" height="471" alt="Screenshot 2025-08-31 192829" src="https://github.com/user-attachments/assets/eb99ea52-d712-4818-a7bb-9e4f25c067b4" />


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
<img width="690" height="185" alt="Screenshot 2025-09-01 191447" src="https://github.com/user-attachments/assets/ef25341d-8fb7-4c4b-855f-66bb431550f4" />

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
<img width="622" height="151" alt="Screenshot 2025-09-01 192212" src="https://github.com/user-attachments/assets/c86c1e65-8073-4543-8b0a-199f3257b3e9" />

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
<img width="622" height="151" alt="Screenshot 2025-09-01 192212" src="https://github.com/user-attachments/assets/b879b637-cd54-4749-be7e-5b13609eaa64" />


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
<img width="622" height="151" alt="Screenshot 2025-09-01 192212" src="https://github.com/user-attachments/assets/e3da6377-bf3d-424b-a067-66124e87011f" />

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
 <img width="622" height="151" alt="Screenshot 2025-09-01 192212" src="https://github.com/user-attachments/assets/666e4775-603f-424c-90c2-127702c0a6b2" />

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
 <img width="622" height="151" alt="Screenshot 2025-09-01 192212" src="https://github.com/user-attachments/assets/30c36c54-f243-4832-8262-19ce15da3003" />

 
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
 
 <img width="622" height="151" alt="Screenshot 2025-09-01 192212" src="https://github.com/user-attachments/assets/c61fc222-7a48-4e13-afa5-582597be26b9" />

 
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
 <img width="653" height="299" alt="image" src="https://github.com/user-attachments/assets/e0fc7222-f2ea-4992-a243-74e6cd6e0c28" />

 
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
<img width="622" height="222" alt="image" src="https://github.com/user-attachments/assets/8bdd60e5-c26c-4993-9386-4c54dee37c60" />

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
<img width="622" height="222" alt="image" src="https://github.com/user-attachments/assets/d1355dbb-9f70-4cc0-b531-1b7943a95c85" />

 
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
 <img width="637" height="302" alt="image" src="https://github.com/user-attachments/assets/bcbfebde-bce3-42e9-802b-1239c199f129" />

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
<img width="653" height="299" alt="image" src="https://github.com/user-attachments/assets/e0fc7222-f2ea-4992-a243-74e6cd6e0c28" />
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
<img width="461" height="300" alt="image" src="https://github.com/user-attachments/assets/40ee67f3-d453-44ba-a327-62558bd6d875" />


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
<img width="400" height="226" alt="image" src="https://github.com/user-attachments/assets/3a0e0d5e-fdc0-4b1c-ad9c-6ba533de9a08" />

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
<img width="445" height="233" alt="image" src="https://github.com/user-attachments/assets/77776de6-949a-4a46-a2e0-59de1ef1d0ad" />

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

 <img width="435" height="376" alt="image" src="https://github.com/user-attachments/assets/98b3dd1c-6f7f-4384-8b01-8c9a6642cd14" />

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
 <img width="369" height="175" alt="image" src="https://github.com/user-attachments/assets/b136200d-7386-487a-b14e-b705e4865869" /> 

cat forcontinue.sh 
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
 <img width="390" height="230" alt="image" src="https://github.com/user-attachments/assets/e2c8d687-df10-42b4-9499-fa6bfeb74af5" />

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

<img width="412" height="158" alt="image" src="https://github.com/user-attachments/assets/381c8972-6d43-4ca1-bde6-8c0c1bdeb725" />

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="427" height="152" alt="image" src="https://github.com/user-attachments/assets/2c7ba546-f13a-4d12-99ec-0e3e55f18a26" />


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

 <img width="424" height="129" alt="image" src="https://github.com/user-attachments/assets/6b3fd3fe-fc9f-4ca4-8f51-f5d9be114993" />


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
 <img width="308" height="174" alt="image" src="https://github.com/user-attachments/assets/90e0690c-dd82-43da-9d17-c9c2f5e626e2" />

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
<img width="307" height="176" alt="image" src="https://github.com/user-attachments/assets/9216b73f-0c06-4fdc-b1bd-a4fd2a5b8f1f" />


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
 
 <img width="356" height="152" alt="image" src="https://github.com/user-attachments/assets/8ec272bc-545a-4086-8bf7-875903072587" />

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
 <img width="433" height="387" alt="image" src="https://github.com/user-attachments/assets/6b7d46e4-9965-40c5-a05e-bbfb6b0f90cb" />

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
<img width="754" height="180" alt="image" src="https://github.com/user-attachments/assets/0a7d142c-007b-43cd-86cc-94c5660c929c" />

<img width="396" height="124" alt="image" src="https://github.com/user-attachments/assets/3d8efde6-c264-471b-aaae-d34e9bf76fea" />

# RESULT:
The Commands are executed successfully.

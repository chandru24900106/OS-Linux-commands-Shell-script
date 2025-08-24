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

<img width="824" height="191" alt="Screenshot from 2025-08-13 11-20-29" src="https://github.com/user-attachments/assets/abbf4f7f-72fe-40f6-8daf-720f377e9257" />



cat < file2
## OUTPUT

<img width="824" height="230" alt="Screenshot from 2025-08-13 11-22-00" src="https://github.com/user-attachments/assets/78d40814-faa5-4593-b167-3ed372d2d1fd" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="764" height="86" alt="Screenshot from 2025-08-13 11-23-35" src="https://github.com/user-attachments/assets/e87d43a0-f934-466f-9be9-bf96110cfcaa" />
 
comm file1 file2
 ## OUTPUT
<img width="749" height="304" alt="Screenshot from 2025-08-13 11-24-24" src="https://github.com/user-attachments/assets/2d32d8c5-c327-4026-9f86-c4bac765682a" />

 
diff file1 file2
## OUTPUT
<img width="754" height="376" alt="Screenshot from 2025-08-13 11-25-20" src="https://github.com/user-attachments/assets/dfcc3427-6d52-4bf7-beef-4b36b6f01929" />


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

<img width="759" height="121" alt="Screenshot from 2025-08-13 11-27-34" src="https://github.com/user-attachments/assets/919cb1e5-4a01-46aa-af99-fa231641efa4" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="760" height="192" alt="Screenshot from 2025-08-13 11-28-40" src="https://github.com/user-attachments/assets/3012f6db-afbb-4f9d-a599-a3677773b0e3" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="851" height="138" alt="Screenshot from 2025-08-13 11-29-45" src="https://github.com/user-attachments/assets/5d16094b-c113-4e27-8093-6d8b70576936" />


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
<img width="813" height="78" alt="Screenshot from 2025-08-13 11-31-54" src="https://github.com/user-attachments/assets/626c0112-93f0-4289-bea9-918af11ec8c0" />



grep hello newfile 
## OUTPUT
<img width="813" height="78" alt="Screenshot from 2025-08-13 11-31-54" src="https://github.com/user-attachments/assets/e5bc8967-92c4-4ded-81f0-35894b64a15c" />




grep -v hello newfile 
## OUTPUT
<img width="842" height="107" alt="Screenshot from 2025-08-13 11-32-58" src="https://github.com/user-attachments/assets/1fbeae22-152a-4560-8049-135409d9cceb" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="985" height="99" alt="Screenshot from 2025-08-13 11-33-39" src="https://github.com/user-attachments/assets/0d91e1b0-47ac-4e77-8e9f-cbcc8cdb29cf" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="1056" height="83" alt="Screenshot from 2025-08-13 11-35-29" src="https://github.com/user-attachments/assets/10cbd51b-6945-471d-8f80-d67804e3dfce" />



grep -R ubuntu /etc
## OUTPUT

<img width="1194" height="553" alt="Screenshot from 2025-08-13 11-43-13" src="https://github.com/user-attachments/assets/94d65185-48d7-41f6-89d3-682ad5ffbbc6" />


grep -w -n world newfile   
## OUTPUT
<img width="900" height="107" alt="Screenshot from 2025-08-13 11-44-11" src="https://github.com/user-attachments/assets/9ca0546a-bb37-4736-88e6-4a784ee3fb09" />


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
<img width="1004" height="110" alt="Screenshot from 2025-08-13 11-46-35" src="https://github.com/user-attachments/assets/6451bf52-3625-4767-a740-8dfd61769761" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="991" height="111" alt="Screenshot from 2025-08-13 11-47-15" src="https://github.com/user-attachments/assets/3fc82c6f-ed21-4cfa-ae19-1ae8a8240f6c" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="621" height="85" alt="Screenshot from 2025-08-17 21-33-28" src="https://github.com/user-attachments/assets/19a02b5c-2213-4653-a8cc-7f8e0e5ffa44" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="627" height="51" alt="Screenshot from 2025-08-17 21-34-07" src="https://github.com/user-attachments/assets/561bbfb8-19e0-4f62-8a3d-5dd143ff40e2" />


egrep '(world$)' newfile 
## OUTPUT
<img width="624" height="69" alt="Screenshot from 2025-08-17 21-34-45" src="https://github.com/user-attachments/assets/1308144d-2ce7-4d32-ba4a-c31c8cd37b11" />



egrep '(World$)' newfile 
## OUTPUT
<img width="627" height="44" alt="Screenshot from 2025-08-17 21-35-30" src="https://github.com/user-attachments/assets/92896511-961b-417a-accf-db5ddc82458e" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="624" height="87" alt="Screenshot from 2025-08-17 21-36-00" src="https://github.com/user-attachments/assets/f28b6666-c6e1-4e83-bbaf-a9bb492516ad" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="625" height="50" alt="Screenshot from 2025-08-17 21-37-11" src="https://github.com/user-attachments/assets/b6a83d8a-a7b1-4df9-a448-251257cdc864" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="627" height="54" alt="Screenshot from 2025-08-17 21-37-46" src="https://github.com/user-attachments/assets/918cd167-e407-4d77-9936-0b11465b1955" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="629" height="69" alt="Screenshot from 2025-08-17 21-38-46" src="https://github.com/user-attachments/assets/b616434d-28cb-4894-acbd-756f7637bbdb" />


egrep l{2} newfile
## OUTPUT

<img width="625" height="76" alt="Screenshot from 2025-08-17 21-39-21" src="https://github.com/user-attachments/assets/cabad768-2058-4e8a-b76b-5035bd277917" />


egrep 's{1,2}' newfile
## OUTPUT 
<img width="627" height="90" alt="Screenshot from 2025-08-17 21-39-59" src="https://github.com/user-attachments/assets/13da1b52-36e8-4420-942f-9deb3c9b4536" />


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

<img width="530" height="52" alt="Screenshot from 2025-08-17 21-41-51" src="https://github.com/user-attachments/assets/3cb88dd3-e89d-454b-96f2-7ba9b9f87d1d" />


sed -n -e '$p' file23
## OUTPUT

<img width="537" height="52" alt="Screenshot from 2025-08-17 21-42-32" src="https://github.com/user-attachments/assets/5ff198b6-38ca-485c-ae22-6a9e1ef81f92" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="589" height="206" alt="Screenshot from 2025-08-17 21-43-21" src="https://github.com/user-attachments/assets/816a165c-e5a3-4aae-bc40-9597ad27bb1a" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="589" height="206" alt="Screenshot from 2025-08-17 21-44-28" src="https://github.com/user-attachments/assets/fa1ac59e-52c7-4a65-aea7-08db240df752" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="619" height="210" alt="Screenshot from 2025-08-17 21-45-15" src="https://github.com/user-attachments/assets/40116365-24e5-4496-b0c2-bb54c9f51c18" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="618" height="142" alt="Screenshot from 2025-08-17 21-45-42" src="https://github.com/user-attachments/assets/2557d371-5e7d-4cdc-9e3d-d10cef67550e" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="612" height="99" alt="Screenshot from 2025-08-17 21-46-12" src="https://github.com/user-attachments/assets/f1dd63ab-c92a-4707-aa7a-97722da81b2e" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="611" height="71" alt="Screenshot from 2025-08-17 21-46-46" src="https://github.com/user-attachments/assets/d9f011ee-b37f-4388-9218-ad32a1bf0a85" />


seq 10 
## OUTPUT

<img width="616" height="247" alt="Screenshot from 2025-08-17 21-47-28" src="https://github.com/user-attachments/assets/67cb5860-bbdf-4e79-9d13-293af7dac415" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="621" height="93" alt="Screenshot from 2025-08-17 21-47-54" src="https://github.com/user-attachments/assets/b72c8442-8068-4119-8592-c45ea5134620" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="621" height="93" alt="Screenshot from 2025-08-17 21-48-22" src="https://github.com/user-attachments/assets/9e2415f6-4ea9-460a-aab7-fa20354b8119" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="623" height="114" alt="Screenshot from 2025-08-17 21-48-56" src="https://github.com/user-attachments/assets/34aa4344-e9e6-47d7-9aef-80f35ce2d897" />




seq 10 | sed '2,9c hello'
## OUTPUT
<img width="619" height="102" alt="Screenshot from 2025-08-17 21-50-01" src="https://github.com/user-attachments/assets/b3f41b36-ce2b-41ce-a7be-fbc0f5539a82" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="615" height="89" alt="Screenshot from 2025-08-17 21-50-30" src="https://github.com/user-attachments/assets/52541564-524f-4da1-94b7-1337915d1547" />



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
<img width="614" height="135" alt="Screenshot from 2025-08-17 21-53-00" src="https://github.com/user-attachments/assets/b121868b-d053-4459-bf5a-97f294cc4aee" />


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
<img width="751" height="236" alt="Screenshot from 2025-08-24 21-21-09" src="https://github.com/user-attachments/assets/c03fdbec-901d-4f36-8ef6-1f2f33467a03" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1114" height="344" alt="Screenshot from 2025-08-24 21-21-52" src="https://github.com/user-attachments/assets/721bd9cd-80a0-42c5-b7ac-8bd093659629" />

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
<img width="961" height="163" alt="Screenshot from 2025-08-24 21-24-42" src="https://github.com/user-attachments/assets/9240b599-1313-48f5-b21e-0bc9a2412e6d" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1146" height="180" alt="Screenshot from 2025-08-24 21-25-09" src="https://github.com/user-attachments/assets/7070856b-140c-4cfb-af15-e1b2bd561e85" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1156" height="342" alt="Screenshot from 2025-08-24 21-25-39" src="https://github.com/user-attachments/assets/a1c5bb50-e5d1-4b73-94bd-a5de448c1b4b" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1156" height="342" alt="Screenshot from 2025-08-24 21-27-22" src="https://github.com/user-attachments/assets/f2a5a4f4-696f-41ec-aa5e-378512f8ad1b" />


tar -xvf backup.tar
## OUTPUT
<img width="1156" height="342" alt="Screenshot from 2025-08-24 21-27-46" src="https://github.com/user-attachments/assets/e05304d9-ea15-4948-8786-67be10bf31b4" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="1146" height="88" alt="Screenshot from 2025-08-24 21-28-28" src="https://github.com/user-attachments/assets/116c2844-dc79-4c25-8619-b27419c41d66" />
 
gunzip backup.tar.gz
## OUTPUT

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1144" height="118" alt="Screenshot from 2025-08-24 21-32-41" src="https://github.com/user-attachments/assets/481fe261-7831-4883-84ec-f72ecb4196b9" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="1159" height="196" alt="Screenshot from 2025-08-24 21-33-52" src="https://github.com/user-attachments/assets/0c38c748-81a2-4042-b8a0-580ab4dc6c02" />


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
<img width="1159" height="196" alt="Screenshot from 2025-08-24 21-36-16" src="https://github.com/user-attachments/assets/af67ebd2-1f7e-4bdb-8662-e3eff059bca7" />

 
ls file1
## OUTPUT
<img width="1159" height="95" alt="Screenshot from 2025-08-24 21-36-46" src="https://github.com/user-attachments/assets/9fec5f2e-bb3b-4501-abea-0108a82f7e19" />

echo $?
## OUTPUT 
<img width="1159" height="95" alt="Screenshot from 2025-08-24 21-37-09" src="https://github.com/user-attachments/assets/dda008f8-d94f-4b8e-8c4c-17d913f8c42a" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="1151" height="233" alt="Screenshot from 2025-08-24 21-37-52" src="https://github.com/user-attachments/assets/a50d7467-373d-4042-8bb3-3042c694b8ca" />

abcd
 
echo $?
 ## OUTPUT
<img width="1148" height="307" alt="Screenshot from 2025-08-24 21-38-26" src="https://github.com/user-attachments/assets/46d18573-c112-488f-9d2c-bafecd41432b" />


 
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

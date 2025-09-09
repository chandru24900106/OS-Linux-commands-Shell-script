# NAME : CHANDRU V
# REG NO : 212224230043
# EX:1
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

<img width="319" height="129" alt="Screenshot 2025-08-26 061602" src="https://github.com/user-attachments/assets/39f308a0-61bd-4903-98b4-bebab907cc12" />


cat < file2
## OUTPUT
<img width="318" height="181" alt="Screenshot 2025-08-26 061616" src="https://github.com/user-attachments/assets/afee8372-49cf-4d47-97cd-7d78dfc0bd0f" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="375" height="79" alt="Screenshot 2025-08-26 061828" src="https://github.com/user-attachments/assets/e973bcb4-5903-48b7-8add-0ca070b7beb0" />

comm file1 file2
 ## OUTPUT

 <img width="377" height="228" alt="Screenshot 2025-08-26 061919" src="https://github.com/user-attachments/assets/e15a9cf1-54d8-467d-a686-d5f263b39ee4" />

diff file1 file2
## OUTPUT

<img width="345" height="305" alt="Screenshot 2025-08-26 061955" src="https://github.com/user-attachments/assets/6b647fde-3039-4934-bd31-0bca32969d39" />

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

<img width="319" height="104" alt="Screenshot 2025-09-01 214259" src="https://github.com/user-attachments/assets/b5dfa38b-8785-4207-8401-22e6e49dcce2" />



cut -d "|" -f 1 file22
## OUTPUT
<img width="298" height="126" alt="Screenshot 2025-09-01 214312" src="https://github.com/user-attachments/assets/08290297-b1a9-4a09-824f-27096221afb7" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="327" height="120" alt="Screenshot 2025-09-01 214323" src="https://github.com/user-attachments/assets/5ddfbd42-d97d-4163-9d8c-07e967c062f0" />

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

<img width="315" height="74" alt="Screenshot 2025-09-01 215157" src="https://github.com/user-attachments/assets/2892d8be-ede4-44ae-a882-2b186cd07935" />


grep hello newfile 
## OUTPUT


<img width="315" height="74" alt="Screenshot 2025-09-01 215157" src="https://github.com/user-attachments/assets/1efc9c78-145d-4e22-8b5e-e5ca9c918c36" />

grep -v hello newfile 
## OUTPUT

<img width="307" height="78" alt="Screenshot 2025-09-01 222735" src="https://github.com/user-attachments/assets/fef6950e-6fea-4fce-984c-f65e58f0d559" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="373" height="104" alt="Screenshot 2025-09-01 222748" src="https://github.com/user-attachments/assets/0f78e7d8-c200-428f-a30d-9c49c4ca737b" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="399" height="70" alt="Screenshot 2025-09-01 222758" src="https://github.com/user-attachments/assets/3e8ef1e9-7f0c-498e-9706-4a387e41564f" />



grep -R ubuntu /etc
## OUTPUT

<img width="806" height="526" alt="Screenshot 2025-09-01 223015" src="https://github.com/user-attachments/assets/c41d32d7-cb7b-49ec-976d-cb9ce563359b" />


grep -w -n world newfile   
## OUTPUT
<img width="400" height="99" alt="Screenshot 2025-09-01 223122" src="https://github.com/user-attachments/assets/e5f0d042-1255-480c-baeb-efd64c422e2b" />


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

<img width="416" height="99" alt="Screenshot 2025-09-01 223447" src="https://github.com/user-attachments/assets/02f6f125-45df-4de7-b6ed-574215c89162" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="458" height="106" alt="Screenshot 2025-09-01 223456" src="https://github.com/user-attachments/assets/8877f2e4-f54e-4671-88ad-4e777c6fb149" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


<img width="422" height="96" alt="Screenshot 2025-09-01 223504" src="https://github.com/user-attachments/assets/9319c89a-15ff-415a-87c0-274c01868286" />


egrep '(^hello)' newfile 
## OUTPUT

<img width="397" height="73" alt="Screenshot 2025-09-01 223518" src="https://github.com/user-attachments/assets/17867b07-8e0e-4b33-9546-2faa2f3cdf4f" />


egrep '(world$)' newfile 
## OUTPUT

<img width="403" height="106" alt="Screenshot 2025-09-01 223528" src="https://github.com/user-attachments/assets/e068a1d8-bde8-4216-8f48-992422238534" />


egrep '(World$)' newfile 
## OUTPUT
<img width="408" height="71" alt="Screenshot 2025-09-01 223537" src="https://github.com/user-attachments/assets/defc6343-a60a-404d-a440-7c5f687351c8" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="365" height="122" alt="Screenshot 2025-09-02 112744" src="https://github.com/user-attachments/assets/c84bf52b-083f-4c52-b974-cbab6f139572" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="378" height="70" alt="Screenshot 2025-09-02 112755" src="https://github.com/user-attachments/assets/e870426f-19ed-466e-add1-57a3363ad114" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="394" height="74" alt="Screenshot 2025-09-02 112807" src="https://github.com/user-attachments/assets/f8c447fe-d7ba-4104-8bc3-347703d79f8b" />

egrep l{2} newfile
## OUTPUT

<img width="345" height="105" alt="Screenshot 2025-09-02 112819" src="https://github.com/user-attachments/assets/ef10b7d9-2fb5-4c14-a2a5-2646ee82cee7" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="379" height="124" alt="Screenshot 2025-09-02 112827" src="https://github.com/user-attachments/assets/37a27a93-6518-4860-a541-bf1c887a6ca1" />

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

<img width="354" height="80" alt="Screenshot 2025-09-02 113326" src="https://github.com/user-attachments/assets/ef594d68-5f9a-48b1-ac2a-5c015d43b853" />


sed -n -e '$p' file23
## OUTPUT

<img width="371" height="66" alt="Screenshot 2025-09-02 113333" src="https://github.com/user-attachments/assets/c0ad8f2f-667a-406c-ab33-87bbbdf2cd8c" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="426" height="246" alt="Screenshot 2025-09-02 113340" src="https://github.com/user-attachments/assets/9156b2c3-6b1b-4cc7-bb70-a25a494e95e0" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="445" height="248" alt="Screenshot 2025-09-02 113401" src="https://github.com/user-attachments/assets/5178e00a-619c-49ef-8373-1fd24e1d9b27" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="419" height="249" alt="Screenshot 2025-09-02 113410" src="https://github.com/user-attachments/assets/ca7860f6-30f4-47e0-a21a-7d120ce4aaca" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="420" height="170" alt="Screenshot 2025-09-02 113427" src="https://github.com/user-attachments/assets/e1e145a9-62a2-4c3c-8edb-d510b3163218" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="406" height="127" alt="Screenshot 2025-09-02 113517" src="https://github.com/user-attachments/assets/9a48ff99-f9fd-4401-9342-0bce2b4b5d7b" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="417" height="99" alt="Screenshot 2025-09-02 113524" src="https://github.com/user-attachments/assets/8e46b0b2-3649-417c-96b6-f89b8bc86fe0" />


seq 10 
## OUTPUT

<img width="349" height="297" alt="Screenshot 2025-09-02 113554" src="https://github.com/user-attachments/assets/68f6392f-5837-429b-8c94-8f6d2e0a38fa" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="385" height="121" alt="Screenshot 2025-09-02 113601" src="https://github.com/user-attachments/assets/7f6b56cc-636f-4026-b521-f2615a1bbf18" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="323" height="122" alt="Screenshot 2025-09-02 113608" src="https://github.com/user-attachments/assets/8cd70269-278a-4f58-a857-cd85bc87b249" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="380" height="143" alt="Screenshot 2025-09-02 113622" src="https://github.com/user-attachments/assets/7a8b4ff8-9e70-4909-9fcb-6be72f28575c" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="449" height="124" alt="Screenshot 2025-09-02 113631" src="https://github.com/user-attachments/assets/57b6a8f8-31b4-45c3-810f-c5e198185511" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="377" height="120" alt="Screenshot 2025-09-02 113641" src="https://github.com/user-attachments/assets/26ec350b-1b8a-4bbd-8d44-3c00c3b58ff2" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="429" height="125" alt="Screenshot 2025-09-02 113653" src="https://github.com/user-attachments/assets/e9ab391b-8c37-4ff5-9e3e-10af317b14b8" />


sed -n '2,4{s/$/*/;p}' file23

<img width="402" height="120" alt="Screenshot 2025-09-02 113702" src="https://github.com/user-attachments/assets/0f206e83-9208-49a2-9c2d-890ae06784dd" />

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
<img width="359" height="170" alt="Screenshot 2025-09-02 113918" src="https://github.com/user-attachments/assets/90e9d484-73eb-4191-a229-a54702bc8cad" />


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

<img width="371" height="173" alt="Screenshot 2025-09-02 113926" src="https://github.com/user-attachments/assets/3f83d913-2bab-46f2-93cf-2bcbc75d270d" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="454" height="248" alt="Screenshot 2025-09-02 114459" src="https://github.com/user-attachments/assets/7bd57271-cb2e-4518-926a-1ac860ed4c6a" />

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

<img width="446" height="124" alt="Screenshot 2025-09-02 114558" src="https://github.com/user-attachments/assets/aff2cc84-dcaa-4649-bbb2-7fd3ea399a8b" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="541" height="118" alt="Screenshot 2025-09-02 114609" src="https://github.com/user-attachments/assets/960511fa-a8dd-42c8-a909-b77e0a9c4149" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="437" height="369" alt="Screenshot 2025-09-02 114626" src="https://github.com/user-attachments/assets/7c7108fa-7056-4afb-a68a-6d6dfcd8add4" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="642" height="522" alt="Screenshot 2025-09-02 114651" src="https://github.com/user-attachments/assets/91869879-2b3c-41f6-afbb-67f6643ecaa4" />


tar -xvf backup.tar
## OUTPUT
<img width="646" height="374" alt="Screenshot 2025-09-02 114705" src="https://github.com/user-attachments/assets/57154e0a-f2b4-4946-84ce-e1eae7f92da5" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="637" height="80" alt="Screenshot 2025-09-02 114725" src="https://github.com/user-attachments/assets/5a468bc4-7f0c-40b6-9f67-663ad31c6725" />

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

 <img width="494" height="272" alt="Screenshot 2025-09-08 103147" src="https://github.com/user-attachments/assets/6e4db45f-9759-48be-a648-0acb8ed47ae6" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="416" height="277" alt="Screenshot 2025-09-08 103638" src="https://github.com/user-attachments/assets/ab054b8e-3c73-4e8d-a167-04738c665722" />


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
<img width="690" height="449" alt="Screenshot 2025-09-08 103701" src="https://github.com/user-attachments/assets/d678e9a0-21d2-4238-9a4f-0e295d1753b3" />

 
ls file1
## OUTPUT
<img width="637" height="73" alt="Screenshot 2025-09-08 103717" src="https://github.com/user-attachments/assets/7d88c12f-4cae-43fb-9215-1cd5bbdf9baf" />

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="350" height="78" alt="Screenshot 2025-09-08 103730" src="https://github.com/user-attachments/assets/244e156c-c7f2-41ac-9a49-1c65545b5fcc" />

echo $?
## OUTPUT 
 <img width="370" height="73" alt="Screenshot 2025-09-08 103739" src="https://github.com/user-attachments/assets/c0938811-be98-48d2-a093-fa49c7985921" />

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



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

<img width="654" height="155" alt="Screenshot 2025-09-08 104151" src="https://github.com/user-attachments/assets/1cec648a-7cc7-4a83-acaa-f6bf65a6ed33" />

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
<img width="642" height="152" alt="Screenshot 2025-09-08 104205" src="https://github.com/user-attachments/assets/737ba254-4e3d-4f17-bcc4-2afcfddc3080" />

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

<img width="638" height="199" alt="Screenshot 2025-09-08 104443" src="https://github.com/user-attachments/assets/5a2a89be-b237-4cd3-8a2f-a59a404bcfd3" />


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
<img width="626" height="174" alt="Screenshot 2025-09-08 104549" src="https://github.com/user-attachments/assets/b2ee2e22-77d4-41a8-962f-3120572da38f" />

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
## OUTPUT
<img width="638" height="199" alt="Screenshot 2025-09-08 104443" src="https://github.com/user-attachments/assets/5007e10d-5458-49f4-9003-8203aae13de4" />

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
<img width="635" height="154" alt="Screenshot 2025-09-08 104803" src="https://github.com/user-attachments/assets/8fbe2802-4f99-41f0-bfa8-90bf7abafeda" />


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
<img width="662" height="156" alt="Screenshot 2025-09-08 104923" src="https://github.com/user-attachments/assets/d753574b-9cf1-4c81-bb60-c0727379d1d1" />

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
 <img width="469" height="132" alt="Screenshot 2025-09-08 105451" src="https://github.com/user-attachments/assets/c0b45db5-fccf-4a29-b768-d4878798b652" />

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
 <img width="630" height="428" alt="Screenshot 2025-09-08 110955" src="https://github.com/user-attachments/assets/927c6859-60fd-49b9-97f1-45b187c08df3" />

 
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
 
 
 <img width="541" height="221" alt="Screenshot 2025-09-08 204620" src="https://github.com/user-attachments/assets/125a6037-cb6d-40e5-87d6-827c8b4b4408" />

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
 <img width="646" height="295" alt="Screenshot 2025-09-08 204631" src="https://github.com/user-attachments/assets/e93401ed-c8c7-4978-848c-9e59d3728e4a" />

 
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
 <img width="623" height="226" alt="Screenshot 2025-09-08 204645" src="https://github.com/user-attachments/assets/97a97df7-b637-44b4-8dbd-2616526d3652" />

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
 <img width="611" height="377" alt="Screenshot 2025-09-08 204657" src="https://github.com/user-attachments/assets/c5571cc9-2f30-4059-8945-06f4275f9842" />

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

<img width="362" height="247" alt="Screenshot 2025-09-09 101614" src="https://github.com/user-attachments/assets/fb9e89bb-6fb0-41cb-b5d7-dcf916e2537d" />

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
<img width="418" height="224" alt="Screenshot 2025-09-09 102516" src="https://github.com/user-attachments/assets/39262bfb-37c6-4cbc-9519-a3a5c88fefc2" />

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
<img width="351" height="224" alt="Screenshot 2025-09-09 104016" src="https://github.com/user-attachments/assets/8637b08d-6561-485f-95eb-e16541ca1ed3" />

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

<img width="527" height="407" alt="Screenshot 2025-09-09 104438" src="https://github.com/user-attachments/assets/e4767224-5384-4ee4-80db-9e6872c9fc03" />
 

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
 <img width="453" height="372" alt="Screenshot 2025-09-09 105400" src="https://github.com/user-attachments/assets/f418ecc1-6692-4db1-acce-368feac46e95" />

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
### OUTPUT 
<img width="417" height="227" alt="image" src="https://github.com/user-attachments/assets/d6605c00-4d0a-48ec-b538-34f4e47557e6" />



# RESULT:
The Commands are executed successfully.

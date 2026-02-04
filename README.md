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
![WhatsApp Image 2026-01-30 at 9 33 00 AM](https://github.com/user-attachments/assets/b772d953-3b5b-4acd-b0ec-cfbd2f06a011)



cat < file2
## OUTPUT
<img width="375" height="180" alt="Screenshot 2026-01-30 093402" src="https://github.com/user-attachments/assets/9408d604-b627-45d7-b614-1f533f10b1df" />


# Comparing Files
cmp file1 file2
## OUTPUT
 ![WhatsApp Image 2026-01-30 at 9 36 44 AM](https://github.com/user-attachments/assets/b3194ffe-75ee-4a04-a9d5-0f2f49ed7e5a)

comm file1 file2
 ## OUTPUT
<img width="465" height="243" alt="image" src="https://github.com/user-attachments/assets/58cdcf69-a5a7-40a5-ba48-aa3fad0e1594" />

 
diff file1 file2
## OUTPUT
<img width="502" height="309" alt="image" src="https://github.com/user-attachments/assets/60f51512-57e2-49e5-a2be-a69d5268567f" />


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
<img width="401" height="93" alt="image" src="https://github.com/user-attachments/assets/d6e737fa-e78e-4318-aa21-af7ee514dc9c" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="455" height="118" alt="image" src="https://github.com/user-attachments/assets/b4b4b1be-f176-451a-b7e1-9439e7707644" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="459" height="121" alt="image" src="https://github.com/user-attachments/assets/75bd6332-3319-4031-9cb0-b37f37f15d65" />

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
<img width="457" height="60" alt="image" src="https://github.com/user-attachments/assets/bd634b15-23f3-4306-a868-618db1007eff" />



grep hello newfile 
## OUTPUT
<img width="456" height="60" alt="image" src="https://github.com/user-attachments/assets/b46667cc-fe1f-4160-b58c-868986c32eaf" />




grep -v hello newfile 
## OUTPUT
<img width="463" height="71" alt="image" src="https://github.com/user-attachments/assets/255b1315-a1b6-4832-86be-80d2a3daea82" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="587" height="86" alt="image" src="https://github.com/user-attachments/assets/9c5f1eb5-f252-4930-b041-375c90c637d5" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="611" height="64" alt="image" src="https://github.com/user-attachments/assets/ed6be920-8158-4c66-b723-b4353a2c4ace" />




grep -R ubuntu /etc
## OUTPUT
<img width="707" height="220" alt="image" src="https://github.com/user-attachments/assets/957b50b7-fdfc-48f1-8902-6687db8b750c" />



grep -w -n world newfile   
## OUTPUT
<img width="643" height="89" alt="image" src="https://github.com/user-attachments/assets/ee523717-c39e-4b38-96a2-1ef246356bc5" />


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
<img width="653" height="86" alt="image" src="https://github.com/user-attachments/assets/b2786ef4-20f9-46a0-acfd-52f5f75cb1df" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="643" height="82" alt="image" src="https://github.com/user-attachments/assets/9befac33-5e7f-4fad-9947-f6e4917bf1d8" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="652" height="90" alt="image" src="https://github.com/user-attachments/assets/1d4d1d10-b9d9-4937-8803-3b316ce74a7d" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="607" height="68" alt="image" src="https://github.com/user-attachments/assets/8707033b-7e3d-4617-a152-d8bd84b0f227" />



egrep '(world$)' newfile 
## OUTPUT
<img width="640" height="54" alt="image" src="https://github.com/user-attachments/assets/0568fbef-2d47-4718-912d-70b325dec2ce" />



egrep '(World$)' newfile 
## OUTPUT
<img width="665" height="63" alt="image" src="https://github.com/user-attachments/assets/013e1b6d-b89a-4ade-b271-61179d00ed05" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="588" height="85" alt="image" src="https://github.com/user-attachments/assets/642b2292-e27e-4129-9c35-e330277b8372" />



egrep '[1-9]' newfile 
## OUTPUT

<img width="672" height="60" alt="image" src="https://github.com/user-attachments/assets/c03487ca-f40d-4a23-ae1f-45167c475810" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="653" height="68" alt="image" src="https://github.com/user-attachments/assets/f15af179-674d-41b0-ae7b-d1134e1728f8" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="635" height="66" alt="image" src="https://github.com/user-attachments/assets/495eed28-ea10-4319-bd46-5a16b5392bcb" />


egrep l{2} newfile
## OUTPUT
<img width="582" height="63" alt="image" src="https://github.com/user-attachments/assets/e3314097-e0d5-4d27-a892-309aafc368a6" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="678" height="87" alt="image" src="https://github.com/user-attachments/assets/dc5d9b00-5f6c-47bf-aa2d-54cc42f5e6f5" />


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
<img width="669" height="116" alt="image" src="https://github.com/user-attachments/assets/bcf28960-e7fc-4a37-86a3-b0345eddbb6f" />



sed -n -e '$p' file23
## OUTPUT
<img width="466" height="57" alt="image" src="https://github.com/user-attachments/assets/4f9dd2e2-7401-429e-a02f-4e2c564c4c74" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="483" height="56" alt="image" src="https://github.com/user-attachments/assets/09dbc782-498c-472d-a826-8a483d571920" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="521" height="235" alt="image" src="https://github.com/user-attachments/assets/c6993ae9-6149-49db-a4f8-f8c71153ab52" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="525" height="248" alt="image" src="https://github.com/user-attachments/assets/a9562e7a-d8c1-42b3-9b60-3661410d62a9" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="578" height="250" alt="image" src="https://github.com/user-attachments/assets/640cb0a5-0450-4880-8bea-83dbdaa73ed6" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="577" height="164" alt="image" src="https://github.com/user-attachments/assets/c5a7ccc8-973d-4e12-9428-6479dc803548" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="535" height="113" alt="image" src="https://github.com/user-attachments/assets/eeb74bfd-6897-4434-b2ac-e54fc9dece72" />



seq 10 
## OUTPUT
<img width="575" height="81" alt="image" src="https://github.com/user-attachments/assets/2e346584-aba3-4077-8006-6eaf1ce85a4d" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="585" height="298" alt="image" src="https://github.com/user-attachments/assets/1f0990b4-3c9c-4af7-8408-cab978ea4a24" />



seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="585" height="119" alt="image" src="https://github.com/user-attachments/assets/b92f7239-3395-4c31-8777-0af78d680cf1" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="538" height="107" alt="image" src="https://github.com/user-attachments/assets/6925f8cc-2c71-461f-8e38-301490f31655" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="545" height="130" alt="image" src="https://github.com/user-attachments/assets/ebbf7d88-4eb7-44b4-b98b-54eb6b836601" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="577" height="110" alt="image" src="https://github.com/user-attachments/assets/288421e9-7b0c-4dc5-85b4-14cf66d823c9" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="577" height="109" alt="image" src="https://github.com/user-attachments/assets/5d119293-a1a3-4302-ada5-9cfc999d6a42" />


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
<img width="534" height="110" alt="image" src="https://github.com/user-attachments/assets/6e3c2900-0565-42ee-afff-adcf97207a09" />


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
<img width="579" height="104" alt="image" src="https://github.com/user-attachments/assets/39de3cad-487e-498b-837c-fb2519c55769" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="580" height="110" alt="image" src="https://github.com/user-attachments/assets/c5eae0e2-5c4e-4bbe-ae7a-06cfd0b1eb3e" />

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
<img width="369" height="173" alt="image" src="https://github.com/user-attachments/assets/b0903b62-4ed4-4178-98f7-50f7060fab77" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="388" height="157" alt="image" src="https://github.com/user-attachments/assets/41df9947-68d3-4782-9522-f45646cff68a" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="658" height="233" alt="image" src="https://github.com/user-attachments/assets/565921b4-7eef-4b85-a590-d7cd56366f2b" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="671" height="111" alt="image" src="https://github.com/user-attachments/assets/e8f08a85-fd6b-4fe0-b745-cf8dd260bca6" />


tar -xvf backup.tar
## OUTPUT
<img width="701" height="116" alt="image" src="https://github.com/user-attachments/assets/d14f8786-27c6-4f56-9634-5ddede4abe93" />

gzip backup.tar

ls .gz
## OUTPUT
 <img width="326" height="141" alt="image" src="https://github.com/user-attachments/assets/0d8e972c-17c3-4b95-9bad-525712499560" />

gunzip backup.tar.gz
## OUTPUT
<img width="467" height="163" alt="image" src="https://github.com/user-attachments/assets/9788014c-4379-4948-9e8b-0b2ad010344c" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="775" height="163" alt="image" src="https://github.com/user-attachments/assets/f2ee56c6-e40b-4741-a53b-abb9e53fc2a9" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="349" height="79" alt="image" src="https://github.com/user-attachments/assets/c7375b6e-1e6f-4d26-8cfa-208a1c01baa9" />


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
<img width="374" height="82" alt="image" src="https://github.com/user-attachments/assets/bc682aed-c81f-41a6-bec8-4f72d5b0fb1e" />

 
ls file1
## OUTPUT
<img width="808" height="130" alt="image" src="https://github.com/user-attachments/assets/e5dbd647-4ba5-405e-9f90-8a4373befb16" />

echo $?
## OUTPUT 
<img width="92" height="38" alt="image" src="https://github.com/user-attachments/assets/69582b4a-7489-4e4e-acf3-2c665b1ba647" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="780" height="158" alt="image" src="https://github.com/user-attachments/assets/d896bf17-46a7-4db7-a67a-5034e8525170" />

abcd
 
echo $?
 ## OUTPUT
<img width="772" height="226" alt="image" src="https://github.com/user-attachments/assets/bc67b893-dcf1-4add-9df5-69966dc23afa" />


 
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
<img width="780" height="317" alt="image" src="https://github.com/user-attachments/assets/21782ba2-9237-4e07-a4ec-066f028e69a7" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="401" height="112" alt="image" src="https://github.com/user-attachments/assets/8c34e376-0f9d-489c-a98c-df83b1b6f199" />


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
<img width="512" height="394" alt="image" src="https://github.com/user-attachments/assets/86b932da-b30f-451b-baca-815f53f32b11" />

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


<img width="325" height="62" alt="image" src="https://github.com/user-attachments/assets/84bf3fcf-be55-40ea-ab85-c55add59324e" />

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
<img width="301" height="67" alt="image" src="https://github.com/user-attachments/assets/b8d78f94-a151-4981-8403-fd0f87851d5a" />

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
<img width="579" height="265" alt="image" src="https://github.com/user-attachments/assets/f6d3ab8b-2bc7-4f53-8408-2e454d05ea1c" />

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
<img width="585" height="293" alt="image" src="https://github.com/user-attachments/assets/1889bab1-ea10-40b8-82fb-b659ec43ebcc" />


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
<img width="467" height="226" alt="Screenshot 2026-02-04 084119" src="https://github.com/user-attachments/assets/04578d15-a651-40f6-a001-3f818a90d211" />


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
<img width="739" height="305" alt="image" src="https://github.com/user-attachments/assets/f34b5cb7-fb3b-4564-8877-b3499137c303" />

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
<img width="467" height="226" alt="Screenshot 2026-02-04 084119" src="https://github.com/user-attachments/assets/bc6e7ca2-4a13-407c-951b-d04d32be70bf" />


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
<img width="467" height="226" alt="Screenshot 2026-02-04 084119" src="https://github.com/user-attachments/assets/469fab1b-8ced-4f7d-9fc4-f4a090d73125" />

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
<img width="467" height="226" alt="Screenshot 2026-02-04 084119" src="https://github.com/user-attachments/assets/315ed1e5-4a95-4b8a-92b0-8c6ea985fb46" />

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
<img width="467" height="226" alt="Screenshot 2026-02-04 084119" src="https://github.com/user-attachments/assets/cb794258-b0a5-4700-b821-e5028f6fa6f8" />

 
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
<img width="467" height="226" alt="Screenshot 2026-02-04 084119" src="https://github.com/user-attachments/assets/6e509607-be98-4247-a9b2-713313e965de" />

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
 <img width="467" height="226" alt="Screenshot 2026-02-04 084119" src="https://github.com/user-attachments/assets/3a581b70-af39-4268-a167-8604dd335919" />

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
<img width="467" height="226" alt="Screenshot 2026-02-04 084119" src="https://github.com/user-attachments/assets/4137b54c-45e4-4e3e-82d1-a42ac89b812b" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

<img width="467" height="226" alt="Screenshot 2026-02-04 084119" src="https://github.com/user-attachments/assets/90e1d811-2b4b-4648-a99c-93dfe5febac3" />


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
<img width="586" height="49" alt="Screenshot 2026-02-04 085058" src="https://github.com/user-attachments/assets/26ed0511-c670-4040-b654-9bb50b3e7573" />

 
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
<img width="395" height="284" alt="Screenshot 2026-02-04 085035" src="https://github.com/user-attachments/assets/f803de58-23ca-48c1-a61b-8781662ce057" />

 
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
<img width="360" height="178" alt="Screenshot 2026-02-04 084958" src="https://github.com/user-attachments/assets/b252faa5-5b79-474b-ab5f-7fb1e9f24269" />


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
<img width="329" height="56" alt="Screenshot 2026-02-04 084917" src="https://github.com/user-attachments/assets/f9992dce-6a4f-44ae-8a98-2e1f7cbb23ba" />


# RESULT:
The Commands are executed successfully.

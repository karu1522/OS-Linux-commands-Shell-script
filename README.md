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
<img width="321" height="164" alt="image" src="https://github.com/user-attachments/assets/f2887d44-47b2-48a5-9640-1505f68f37f0" />



cat < file2
## OUTPUT
<img width="330" height="200" alt="image" src="https://github.com/user-attachments/assets/ff28aed9-84a8-47c6-aec0-9b7675aa4432" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="393" height="71" alt="image" src="https://github.com/user-attachments/assets/5af464f5-e39d-4144-a7ed-ed176ed06b92" />

comm file1 file2
 ## OUTPUT
<img width="347" height="199" alt="image" src="https://github.com/user-attachments/assets/aeadc8e1-cd59-4370-ad96-177fef567e1c" />

 
diff file1 file2
## OUTPUT
<img width="332" height="274" alt="image" src="https://github.com/user-attachments/assets/2e143fc5-07bf-4424-844f-6fc20b1fc889" />


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
<img width="284" height="101" alt="image" src="https://github.com/user-attachments/assets/427b4f07-06d6-409f-ab6a-9b91b246236b" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="313" height="131" alt="image" src="https://github.com/user-attachments/assets/a7d467a2-0340-474c-9693-6333983323a4" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="319" height="140" alt="image" src="https://github.com/user-attachments/assets/c51db44a-27d9-41c8-8ac3-b7479f104f90" />


cat > newfile 
```
Hello world
hello world
^d
````
cat < newfile 
## OUTPUT
<img width="295" height="96" alt="image" src="https://github.com/user-attachments/assets/7322acfe-72ec-4edf-a3d5-e7530c215c64" />

 
grep Hello newfile 
## OUTPUT
<img width="294" height="76" alt="image" src="https://github.com/user-attachments/assets/135fb2ba-1b88-4d47-adc5-46ebbe8aaec9" />




grep hello newfile 
## OUTPUT
<img width="293" height="76" alt="image" src="https://github.com/user-attachments/assets/8b344198-dc86-4c00-9a28-f95da16955ca" />




grep -v hello newfile 
## OUTPUT
<img width="300" height="79" alt="image" src="https://github.com/user-attachments/assets/a3712856-0e31-40b6-896b-2190e3f0006e" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="363" height="103" alt="image" src="https://github.com/user-attachments/assets/c26d461e-ae0a-49fc-aea2-159af20c9e88" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="386" height="76" alt="image" src="https://github.com/user-attachments/assets/171cbb79-5ba0-466c-a66e-1d7ee0525a36" />




grep -R ubuntu /etc
## OUTPUT
<img width="1260" height="326" alt="image" src="https://github.com/user-attachments/assets/b64991be-c688-4b45-9e4a-d34a88972bdc" />



grep -w -n world newfile   
## OUTPUT
<img width="308" height="98" alt="image" src="https://github.com/user-attachments/assets/f5e76fa1-6fb3-44d0-b3b1-e2a1628af964" />


cat > newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```

cat < newfile
## OUTPUT
<img width="334" height="176" alt="image" src="https://github.com/user-attachments/assets/02fa1e9f-3846-4bda-b544-66b461051358" />



egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="374" height="97" alt="image" src="https://github.com/user-attachments/assets/8a63f529-20b2-4749-bc30-ff870d185df7" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="362" height="98" alt="image" src="https://github.com/user-attachments/assets/2c5563f4-0c89-4b7c-8321-8fa006cebb4c" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="399" height="100" alt="image" src="https://github.com/user-attachments/assets/faebb5b5-998c-4286-aceb-17c72a988a73" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="316" height="76" alt="image" src="https://github.com/user-attachments/assets/6cd6feeb-cae9-47a0-864e-3a270a8a369a" />



egrep '(world$)' newfile 
## OUTPUT
<img width="306" height="102" alt="image" src="https://github.com/user-attachments/assets/2c23ce85-03a2-413a-ba57-92e788cb1b49" />



egrep '(World$)' newfile 
## OUTPUT
<img width="319" height="75" alt="image" src="https://github.com/user-attachments/assets/8f82f258-8fb5-4f86-8e16-d4904002dbfa" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="349" height="124" alt="image" src="https://github.com/user-attachments/assets/98652329-acdb-4abf-a7df-e3c3c5728ea9" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="307" height="76" alt="image" src="https://github.com/user-attachments/assets/f5103f08-ff8e-477d-bcef-9463cf3cffaf" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="354" height="76" alt="image" src="https://github.com/user-attachments/assets/64c00953-8864-478b-a53b-e8c42b021d66" />



egrep 'Linux.*World' newfile 
## OUTPUT
<img width="359" height="75" alt="image" src="https://github.com/user-attachments/assets/a78c983b-ec16-4e00-a6a5-96fba75628af" />



egrep l{2} newfile
## OUTPUT
<img width="315" height="102" alt="image" src="https://github.com/user-attachments/assets/e791fbb1-8330-4fa7-95c3-ae2e90a820a1" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="312" height="124" alt="image" src="https://github.com/user-attachments/assets/730cef40-f263-44cc-8f54-1add53f71f60" />


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
<img width="313" height="74" alt="image" src="https://github.com/user-attachments/assets/910e7f96-9654-405f-9991-0c66210ded36" />



sed -n -e '$p' file23
## OUTPUT
<img width="299" height="72" alt="image" src="https://github.com/user-attachments/assets/2490986b-54d0-448b-8618-01f57f25bf00" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="356" height="247" alt="image" src="https://github.com/user-attachments/assets/42eae542-97ca-4031-b27b-1ef6410e0f9e" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="358" height="249" alt="image" src="https://github.com/user-attachments/assets/11adc401-48a5-43ee-a0be-b8829a80127a" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="389" height="246" alt="image" src="https://github.com/user-attachments/assets/509a5cbc-f708-49e5-bc4c-88397a0bf93c" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="318" height="175" alt="image" src="https://github.com/user-attachments/assets/97f2309c-79a9-431f-a8f2-375b337b2fd8" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="346" height="125" alt="image" src="https://github.com/user-attachments/assets/adc4b439-c8c5-4c5f-b20e-32f0a446b28f" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="387" height="101" alt="image" src="https://github.com/user-attachments/assets/ec582094-2df1-4068-bad9-ebda98d4f35b" />



seq 10 
## OUTPUT
<img width="301" height="297" alt="image" src="https://github.com/user-attachments/assets/f9bf1e61-aec1-4e78-a9ba-96ddc6e1f973" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="300" height="123" alt="image" src="https://github.com/user-attachments/assets/88a1cc0b-32da-4a4c-917c-a99a9c32705a" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="308" height="120" alt="image" src="https://github.com/user-attachments/assets/bb1d112d-c3c0-470b-a421-5d66d8a668f2" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="306" height="146" alt="image" src="https://github.com/user-attachments/assets/7131e2ac-4c2e-44da-b7fb-f21b35fb11ec" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="304" height="123" alt="image" src="https://github.com/user-attachments/assets/c67852a6-c34b-4d4e-9a18-b49f878e4407" />



seq 10 | sed '2,9c hello'
## OUTPUT
<img width="316" height="124" alt="image" src="https://github.com/user-attachments/assets/26457bb6-65bd-4c48-9285-a3d72e538d43" />



sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="365" height="126" alt="image" src="https://github.com/user-attachments/assets/7fead8f3-f1dd-4a96-9e17-828d0c445299" />



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
<img width="320" height="174" alt="image" src="https://github.com/user-attachments/assets/838cfb45-d559-4b27-b1db-6b14ebc091a0" />



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
<img width="316" height="176" alt="image" src="https://github.com/user-attachments/assets/fb4d8bad-e2b4-4def-a0b2-0a1d6f264507" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="427" height="250" alt="image" src="https://github.com/user-attachments/assets/503e7639-29e4-4114-bfe0-b3649ceb221b" />


cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
<img width="328" height="123" alt="image" src="https://github.com/user-attachments/assets/ce3922f3-adeb-45d8-bf8f-88cdfa04be9a" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="467" height="120" alt="image" src="https://github.com/user-attachments/assets/950f33aa-b663-49bf-84b2-1792f5f89a06" />



# Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="309" height="250" alt="image" src="https://github.com/user-attachments/assets/2a1d8ad9-90e2-4ed0-89d8-a257ab3d5627" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="608" height="249" alt="image" src="https://github.com/user-attachments/assets/b52db638-a716-4d7d-b1ee-d4436cd97b67" />


tar -xvf backup.tar
## OUTPUT
<img width="403" height="251" alt="image" src="https://github.com/user-attachments/assets/487a10ad-9fbd-4b1d-a636-88fc9deb00f1" />

gzip backup.tar

ls .gz
 
gunzip backup.tar.gz

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
$ chmod 755 my-script.sh
$ ./my-script.sh

## OUTPUT
<img width="548" height="226" alt="image" src="https://github.com/user-attachments/assets/f6803048-7103-4d9d-bb06-61d94fb2520d" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="410" height="122" alt="image" src="https://github.com/user-attachments/assets/7c8e32ab-81d9-47cf-8f7e-dbef9b32c9f7" />


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
 
$ chmod 777 scriptest.sh
 
$ ./scriptest.sh 1 2 3

## OUTPUT
<img width="609" height="449" alt="image" src="https://github.com/user-attachments/assets/87e510eb-905a-4313-bc43-ced95d5007f1" />

 
ls file1
## OUTPUT
<img width="399" height="75" alt="image" src="https://github.com/user-attachments/assets/035dcdd5-a28b-46e8-a5da-cdc1860f13a6" />



echo $?
## OUTPUT 
<img width="407" height="85" alt="image" src="https://github.com/user-attachments/assets/0f345bf8-be7c-45dd-ba00-fa2d292e9660" />

 
abcd
 
echo $?
 ## OUTPUT
<img width="456" height="150" alt="image" src="https://github.com/user-attachments/assets/7cb969bf-9b97-404a-9daf-71a3e0e251d0" />


 
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
<img width="404" height="275" alt="image" src="https://github.com/user-attachments/assets/59c2bc60-e6c3-4815-9294-3c4906231019" />



$ chmod 755 strcomp.sh
 
$ ./strcomp.sh 

## OUTPUT
<img width="616" height="98" alt="image" src="https://github.com/user-attachments/assets/c9b9b153-ee55-4794-ad5b-0bdd94a92aa0" />


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
$ ./psswdperm.sh

## OUTPUT
<img width="430" height="76" alt="image" src="https://github.com/user-attachments/assets/3678226d-f4db-4320-9eb6-84260bbed8e2" />


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

$ ./ifnested.sh

## OUTPUT
<img width="440" height="76" alt="image" src="https://github.com/user-attachments/assets/491cf222-9f91-4821-92c7-d6223916d3fb" />



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
<img width="615" height="122" alt="image" src="https://github.com/user-attachments/assets/8ce74a63-fe88-4118-87a7-aa6039dd1d66" />

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
<img width="627" height="149" alt="image" src="https://github.com/user-attachments/assets/7903146c-6bca-4972-9f53-5bed128234a8" />



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
<img width="635" height="98" alt="image" src="https://github.com/user-attachments/assets/8618cd68-2b2e-4df0-93e6-abd476748f9b" />


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
<img width="642" height="99" alt="image" src="https://github.com/user-attachments/assets/f1a46d67-4a09-422c-9c14-8f9519863693" />



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
 <img width="410" height="297" alt="image" src="https://github.com/user-attachments/assets/37780d53-32ba-4762-9c18-937988cf4e0f" />

 
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
$ ./untiltest.sh

 ## OUTPUT
 <img width="516" height="173" alt="image" src="https://github.com/user-attachments/assets/b1405aef-be7f-4297-9ccc-ba92aba61ff6" />

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
$ ./forin1.sh

## OUTPUT
<img width="606" height="245" alt="image" src="https://github.com/user-attachments/assets/ab237049-b1ae-4abb-a584-15d91c41320f" />

 
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
<img width="596" height="174" alt="image" src="https://github.com/user-attachments/assets/10d46296-74fe-489e-963d-857175edfe06" />

 
cat forin3.sh 
```bash
\#!/bin/bash
\# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ chmod 755 forin3.sh
$ ./forin3.sh 

 ## OUTPUT
 <img width="603" height="250" alt="image" src="https://github.com/user-attachments/assets/f0c6958c-416b-4bbe-a190-9e6db7527ed2" />

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
$ ./forin1.sh

## OUTPUT
<img width="438" height="198" alt="image" src="https://github.com/user-attachments/assets/ebf55f6e-69d1-41a7-9dac-eef158b5211b" />



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
<img width="411" height="228" alt="image" src="https://github.com/user-attachments/assets/4a80c7b9-511f-472b-8532-0c9888c7545e" />


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
<img width="400" height="172" alt="image" src="https://github.com/user-attachments/assets/b3d50c2d-c2de-424a-a9dc-d905e867c06e" />



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
$ ./forctype.sh 
## OUTPUT
<img width="421" height="173" alt="image" src="https://github.com/user-attachments/assets/da61865d-9d03-4839-92ed-00f30c1c1968" />

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
<img width="400" height="350" alt="image" src="https://github.com/user-attachments/assets/53d80f97-e836-408f-ba5c-bef0d3e7a41b" />

 
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

$ chmod 755 forbreak.sh
 
$ ./forbreak.sh 

## OUTPUT
<img width="403" height="99" alt="image" src="https://github.com/user-attachments/assets/85c65ceb-2dd8-4972-8f52-75af04d4ad14" />


 
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
<img width="395" height="149" alt="image" src="https://github.com/user-attachments/assets/30423615-b950-4295-9520-0a1864ce535e" />


 
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
<img width="404" height="102" alt="image" src="https://github.com/user-attachments/assets/0e28432e-70a8-4cbb-a52b-8c3c9bc1d47a" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program."
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh

## OUTPUT
<img width="413" height="99" alt="image" src="https://github.com/user-attachments/assets/e98f5080-ed5b-472d-b8d7-3fa40696197d" />

 
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
./funcex.sh 

./funcex.sh 1 2

## OUTPUT
 <img width="401" height="76" alt="image" src="https://github.com/user-attachments/assets/952e002b-57e2-457e-86ef-548c331bb261" />


 
cat argshift.sh
```bash
#!/bin/bash 
 while (( "$#" )); do 
  echo $1 
  shift 
done
```
$ chmod 777 argshift.sh
$ ./argshift.sh 1 2 3

## OUTPUT
<img width="441" height="150" alt="image" src="https://github.com/user-attachments/assets/6b7fc6c9-9b39-4d39-82a2-5986aa6b2038" />

 
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
$ ./argshift.sh 1 2 3

## OUTPUT
<img width="450" height="143" alt="image" src="https://github.com/user-attachments/assets/986467ee-97a3-4b65-a80d-fcc4ec344b4a" />

 
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

 ./argshift.sh 1 2 3
 
## OUTPUT
<img width="436" height="401" alt="image" src="https://github.com/user-attachments/assets/f73c7500-fb3f-4e32-b9cd-5ad5b29c05ee" />

 
 
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
<img width="412" height="373" alt="image" src="https://github.com/user-attachments/assets/b767983d-d49c-4f34-96d8-a8760be96407" />


 
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
<img width="388" height="123" alt="image" src="https://github.com/user-attachments/assets/d2bea1f5-e37e-41b6-a3da-7ee505252c25" />


# RESULT:
The Commands are executed successfully.

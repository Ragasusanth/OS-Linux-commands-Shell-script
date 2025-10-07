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

<img width="302" height="160" alt="image" src="https://github.com/user-attachments/assets/0ef5e28d-a46c-4808-83ff-78d59de64f92" />

cat < file2
## OUTPUT
<img width="326" height="206" alt="image" src="https://github.com/user-attachments/assets/2833491f-2159-4acf-94f6-d208699d86ac" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="378" height="73" alt="image" src="https://github.com/user-attachments/assets/dd2c09f5-5db4-47d9-bb53-c9aa949bc026" />
 
comm file1 file2
 ## OUTPUT
 
<img width="470" height="351" alt="image" src="https://github.com/user-attachments/assets/efaaa2d1-4323-4179-853a-8068698a468f" />

 
diff file1 file2
## OUTPUT

<img width="342" height="350" alt="image" src="https://github.com/user-attachments/assets/cf64f862-003b-4a30-acba-910d5f4b65f7" />


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

<img width="292" height="117" alt="image" src="https://github.com/user-attachments/assets/203dda14-ab6e-428a-a6d8-cdf2ec282bd8" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="333" height="136" alt="image" src="https://github.com/user-attachments/assets/ef4222f2-00a3-4b6c-8a80-954ab83e829a" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="323" height="152" alt="image" src="https://github.com/user-attachments/assets/43fbfffb-2fd8-4d2f-b14b-be0ec8c218ac" />


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

<img width="340" height="83" alt="image" src="https://github.com/user-attachments/assets/bfb5f6a1-5016-49b4-8c61-6f0993277752" />


grep hello newfile 
## OUTPUT

<img width="331" height="77" alt="image" src="https://github.com/user-attachments/assets/b47ebebf-4f61-4805-8250-7d0ccb2d7c3b" />


grep -v hello newfile 
## OUTPUT

<img width="326" height="72" alt="image" src="https://github.com/user-attachments/assets/08100e00-d199-4766-81f7-511efd8bb866" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="392" height="112" alt="image" src="https://github.com/user-attachments/assets/c3a41b55-cc35-4da9-92ad-bdbae37231a9" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="417" height="76" alt="image" src="https://github.com/user-attachments/assets/b3d41cb3-a614-4dd7-9c9d-37057e3f5452" />

grep -R ubuntu /etc
## OUTPUT

<img width="812" height="496" alt="image" src="https://github.com/user-attachments/assets/b7971183-d579-485f-aef4-7012a484c5c2" />


grep -w -n world newfile   
## OUTPUT

<img width="807" height="276" alt="image" src="https://github.com/user-attachments/assets/805aa045-dc6c-4680-aafd-5a5050058515" />


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

<img width="395" height="105" alt="image" src="https://github.com/user-attachments/assets/466d19c7-b795-44bb-af62-c5523d6cad23" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="406" height="103" alt="image" src="https://github.com/user-attachments/assets/7c4fff0e-4cae-4b58-b4e9-78d46f140e1f" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="442" height="102" alt="image" src="https://github.com/user-attachments/assets/23ea0559-9621-4e32-ae0b-33ed332c4a8e" />

egrep '(^hello)' newfile 
## OUTPUT

<img width="345" height="72" alt="image" src="https://github.com/user-attachments/assets/114d9a11-ee99-479e-a3f7-3cd266a39e6d" />

egrep '(world$)' newfile 
## OUTPUT

<img width="367" height="103" alt="image" src="https://github.com/user-attachments/assets/c5a13f04-4d27-45e8-93b0-49f7636f8b9e" />

egrep '(World$)' newfile 
## OUTPUT

<img width="362" height="81" alt="image" src="https://github.com/user-attachments/assets/f962b203-b012-4e26-bf6b-2f07bd5c4f6f" />

egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="382" height="127" alt="image" src="https://github.com/user-attachments/assets/d4f92ca5-ab4b-4c6d-92b9-12efa388a1cf" />

egrep '[1-9]' newfile 
## OUTPUT

<img width="325" height="72" alt="image" src="https://github.com/user-attachments/assets/2405d28f-ccb6-48a8-8390-92fd0051cfa9" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="382" height="76" alt="image" src="https://github.com/user-attachments/assets/f74a703f-2602-4e90-ac19-e2a04630af61" />

egrep 'Linux.*World' newfile 
## OUTPUT

<img width="385" height="78" alt="image" src="https://github.com/user-attachments/assets/3a03d0e2-af4f-4263-854a-f16eb108ee81" />

egrep l{2} newfile
## OUTPUT

<img width="312" height="100" alt="image" src="https://github.com/user-attachments/assets/08300ae7-860d-4258-b3fe-94fc4adb8935" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="342" height="125" alt="image" src="https://github.com/user-attachments/assets/fb0ee003-2848-49c8-9a65-ed34b67f5926" />


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

<img width="308" height="73" alt="image" src="https://github.com/user-attachments/assets/71f8254d-abfa-4df7-abfa-24c0a11411a6" />


sed -n -e '$p' file23
## OUTPUT

<img width="291" height="83" alt="image" src="https://github.com/user-attachments/assets/fd15846a-9b65-4eef-aad0-f05d9ad23aef" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="396" height="257" alt="image" src="https://github.com/user-attachments/assets/c8e51d8d-ae61-4135-baef-8fae9941b006" />

sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="435" height="257" alt="image" src="https://github.com/user-attachments/assets/59e1ac23-2b18-4eda-aeda-3695d4221ab5" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="417" height="251" alt="image" src="https://github.com/user-attachments/assets/1d8cc891-e378-455d-92e5-8303ee7403ce" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="350" height="177" alt="image" src="https://github.com/user-attachments/assets/e602aee6-4bb6-4357-b7fc-8c5949af806c" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="466" height="125" alt="image" src="https://github.com/user-attachments/assets/18b9cb42-3273-4bf5-834d-68ab65c73cc9" />


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="407" height="105" alt="image" src="https://github.com/user-attachments/assets/3bec1297-0f8a-499f-ae55-186c7bddbbce" />


seq 10 
## OUTPUT

<img width="298" height="298" alt="image" src="https://github.com/user-attachments/assets/fc83d234-f415-4138-994e-1f20844f4ced" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="312" height="128" alt="image" src="https://github.com/user-attachments/assets/207246c0-dcd2-446f-9065-6fece5fb46a7" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="328" height="125" alt="image" src="https://github.com/user-attachments/assets/a1d7b552-0d03-45a1-99ce-da8efdbc6790" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="416" height="152" alt="image" src="https://github.com/user-attachments/assets/bd63e46e-a804-4b43-bc71-d899a750c397" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="353" height="122" alt="image" src="https://github.com/user-attachments/assets/a9cf3272-9af3-4035-9ef6-bc99bb5c5b45" />

seq 10 | sed '2,9c hello'
## OUTPUT

<img width="367" height="125" alt="image" src="https://github.com/user-attachments/assets/94e9e94a-c158-432d-9fb1-9022fb58d5b9" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="408" height="127" alt="image" src="https://github.com/user-attachments/assets/4fe5a41d-f0b2-495b-84da-531d1ecb5912" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="386" height="127" alt="image" src="https://github.com/user-attachments/assets/cb89421b-3744-411d-87c6-52ae8ff6a28d" />


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

<img width="387" height="180" alt="image" src="https://github.com/user-attachments/assets/4c693816-596c-4ae4-8044-c846ab7731de" />


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

<img width="392" height="181" alt="image" src="https://github.com/user-attachments/assets/850508d9-ea36-4434-88b3-5cb7deca1012" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="461" height="252" alt="image" src="https://github.com/user-attachments/assets/ec27f3a3-fb0d-4349-996f-3ce2db0832e9" />


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

<img width="366" height="128" alt="image" src="https://github.com/user-attachments/assets/7a361b8c-0766-4cb2-a7c9-926abd852591" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="477" height="127" alt="image" src="https://github.com/user-attachments/assets/b88d02a2-6816-461e-ab64-8f147daf810f" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="587" height="571" alt="image" src="https://github.com/user-attachments/assets/e2e82876-4685-4d27-93b1-b1db9ebf1133" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="717" height="580" alt="image" src="https://github.com/user-attachments/assets/f72abade-97a5-4c47-b0b3-e62ec943842a" />


tar -xvf backup.tar
## OUTPUT

<img width="556" height="601" alt="image" src="https://github.com/user-attachments/assets/6ea5ee40-e5f6-428b-ab2d-aa815f7bc2d7" />

gzip backup.tar

ls .gz
## OUTPUT

 <img width="518" height="131" alt="image" src="https://github.com/user-attachments/assets/252fa806-89d7-482c-9d03-234c343ba726" />

gunzip backup.tar.gz
## OUTPUT

<img width="485" height="58" alt="image" src="https://github.com/user-attachments/assets/b920ce63-323f-4eff-b952-97ce92e4b2eb" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="527" height="81" alt="image" src="https://github.com/user-attachments/assets/7988f17e-4d1c-49b0-a838-3e7040b5d6af" />



 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="417" height="132" alt="image" src="https://github.com/user-attachments/assets/25f35ade-6bf8-46ba-902f-166287f36a05" />

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

<img width="638" height="401" alt="image" src="https://github.com/user-attachments/assets/25f8eb3b-a310-4fc1-a608-71045b2f5d33" />
 
ls file1
## OUTPUT

<img width="477" height="73" alt="image" src="https://github.com/user-attachments/assets/d260cce4-d95e-4653-ba39-fcdda8bbe567" />

echo $?
## OUTPUT 

<img width="427" height="80" alt="image" src="https://github.com/user-attachments/assets/3133d5a3-7dbb-41a6-8536-cf40797ace23" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 

<img width="510" height="82" alt="image" src="https://github.com/user-attachments/assets/780db3df-4aa6-438a-b7e3-bcd9c523aa8b" />

abcd
 
echo $?
 ## OUTPUT

<img width="510" height="82" alt="image" src="https://github.com/user-attachments/assets/780db3df-4aa6-438a-b7e3-bcd9c523aa8b" />
 
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

<img width="635" height="106" alt="image" src="https://github.com/user-attachments/assets/9c77dc5d-21db-4792-b29f-22013c5a79cf" />


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

<img width="533" height="82" alt="image" src="https://github.com/user-attachments/assets/8452b14e-e831-439a-ab7e-51d41cd6458e" />

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

<img width="416" height="83" alt="image" src="https://github.com/user-attachments/assets/182061cc-9ebd-41a7-b3b5-d1109c04eb2b" />



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

<img width="506" height="156" alt="image" src="https://github.com/user-attachments/assets/d226dcba-6323-4786-9013-721c6c602a6a" />

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

<img width="676" height="146" alt="image" src="https://github.com/user-attachments/assets/ce507048-f0bb-4319-96db-46f77b4c98f4" />

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

<img width="386" height="55" alt="image" src="https://github.com/user-attachments/assets/c4776ac0-475d-4cbb-be72-28bda19c5538" />

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

<img width="385" height="232" alt="image" src="https://github.com/user-attachments/assets/8456b824-747d-446d-8c01-c011e5faab5e" />

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

<img width="602" height="400" alt="image" src="https://github.com/user-attachments/assets/5a146347-db35-4d04-a3d3-70ca21da49b5" />

 
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

<img width="425" height="155" alt="image" src="https://github.com/user-attachments/assets/812abff6-36c0-4565-81f2-e296c3898915" />

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

<img width="782" height="153" alt="image" src="https://github.com/user-attachments/assets/f0eaed9a-a42b-4e8a-b203-0b5e6873ba20" />

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

<img width="453" height="156" alt="image" src="https://github.com/user-attachments/assets/85e392e9-5c52-452c-9da2-329db66ab8ce" />


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

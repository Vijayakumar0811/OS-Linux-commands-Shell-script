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

<img width="699" height="148" alt="Screenshot 2025-08-26 103708" src="https://github.com/user-attachments/assets/1eb1533b-261c-411d-a36c-fbf3c539cebf" />


cat < file2
## OUTPUT
<img width="683" height="169" alt="Screenshot 2025-08-26 103953" src="https://github.com/user-attachments/assets/cc7db5e9-4ff1-45fa-ae2d-905c56e68240" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="734" height="58" alt="Screenshot 2025-08-26 104054" src="https://github.com/user-attachments/assets/4fae5182-4db8-4fc7-b6c4-35bfba565009" />

comm file1 file2
 ## OUTPUT
<img width="758" height="314" alt="Screenshot 2025-08-26 104211" src="https://github.com/user-attachments/assets/3eebc270-fde3-4150-9526-541dc4ddb746" />

 
diff file1 file2
## OUTPUT


<img width="749" height="281" alt="Screenshot 2025-08-26 104250" src="https://github.com/user-attachments/assets/2516c003-f9f2-447d-a8ac-4cab30e2df17" />


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

<img width="751" height="85" alt="Screenshot 2025-08-26 104645" src="https://github.com/user-attachments/assets/6b5bdb9f-db84-4715-8356-679f00e045f5" />




cut -d "|" -f 1 file22
## OUTPUT

<img width="853" height="116" alt="Screenshot 2025-08-26 104728" src="https://github.com/user-attachments/assets/fd398b3e-673a-4135-a52d-9099ea71b780" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="833" height="113" alt="Screenshot 2025-08-26 104807" src="https://github.com/user-attachments/assets/8f4a1021-1faa-4bf2-93d7-38990266a33a" />


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

<img width="779" height="58" alt="Screenshot 2025-08-26 105045" src="https://github.com/user-attachments/assets/f6893eec-61bd-4017-a195-f0082d75dc87" />



grep hello newfile 
## OUTPUT

<img width="775" height="56" alt="Screenshot 2025-08-26 105114" src="https://github.com/user-attachments/assets/9604f24c-b8cd-43e6-86c9-48a22774146b" />




grep -v hello newfile 
## OUTPUT

<img width="820" height="58" alt="Screenshot 2025-08-26 105225" src="https://github.com/user-attachments/assets/0aae88d4-6ac2-4fc1-a5dc-5c32d6dd97b4" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="928" height="88" alt="Screenshot 2025-08-26 105436" src="https://github.com/user-attachments/assets/9e092c61-623d-42e7-abd0-54c6f5d7a91c" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="985" height="57" alt="Screenshot 2025-08-26 105502" src="https://github.com/user-attachments/assets/2f32f63f-0c77-41c0-8ed1-bfe6197b70a4" />




grep -R ubuntu /etc
## OUTPUT
<img width="1919" height="1019" alt="Screenshot 2025-08-26 105708" src="https://github.com/user-attachments/assets/537f8bcb-74aa-400b-97f7-71c22c8fac90" />



grep -w -n world newfile   
## OUTPUT
<img width="851" height="88" alt="Screenshot 2025-08-26 105811" src="https://github.com/user-attachments/assets/5954b252-6602-407e-b440-36a49554aba0" />


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
<img width="945" height="91" alt="Screenshot 2025-08-26 110331" src="https://github.com/user-attachments/assets/da60d33d-0a29-4c64-b5a0-1a6ff9e8e2f7" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="918" height="83" alt="Screenshot 2025-08-26 110414" src="https://github.com/user-attachments/assets/8c0937e8-ea1a-48ea-8ec4-d6d00da4f0a2" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="979" height="89" alt="Screenshot 2025-08-26 110510" src="https://github.com/user-attachments/assets/714937fb-6ae6-4fe5-bc7a-89ca3c620759" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="864" height="58" alt="Screenshot 2025-08-26 110539" src="https://github.com/user-attachments/assets/63ffc5a9-a713-4db6-8569-5909dbaf298f" />



egrep '(world$)' newfile 
## OUTPUT
<img width="862" height="88" alt="Screenshot 2025-08-26 110605" src="https://github.com/user-attachments/assets/50412ad5-b210-4610-b3d1-0a5c05c82480" />



egrep '(World$)' newfile 
## OUTPUT
<img width="864" height="62" alt="Screenshot 2025-08-26 110629" src="https://github.com/user-attachments/assets/bd7b237f-0952-47bb-b30a-770d867896ea" />


egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="917" height="115" alt="Screenshot 2025-08-26 110656" src="https://github.com/user-attachments/assets/60e4b164-5bd2-413e-9122-f64c567ded16" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="824" height="64" alt="Screenshot 2025-08-26 110717" src="https://github.com/user-attachments/assets/482e3f3c-7100-4583-817c-94e3fe76bca1" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="923" height="64" alt="Screenshot 2025-08-26 110741" src="https://github.com/user-attachments/assets/e63ab29a-c85f-4fde-9c23-37b97527038a" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="917" height="60" alt="Screenshot 2025-08-26 110820" src="https://github.com/user-attachments/assets/b1c767e2-6bdb-4f3c-97dc-e705985c01a0" />


egrep l{2} newfile
## OUTPUT
<img width="782" height="83" alt="Screenshot 2025-08-26 110843" src="https://github.com/user-attachments/assets/87d173a9-a762-4dd2-b93c-68c22be97a90" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="838" height="113" alt="Screenshot 2025-08-26 110907" src="https://github.com/user-attachments/assets/82375f22-0c19-4d34-946d-e1c587602d87" />


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
<img width="828" height="312" alt="Screenshot 2025-08-26 111011" src="https://github.com/user-attachments/assets/484f8ab3-31d0-4ec0-b16d-4275897b3197" />



sed -n -e '$p' file23
## OUTPUT

<img width="818" height="58" alt="Screenshot 2025-08-26 111040" src="https://github.com/user-attachments/assets/2b063b99-a722-4a81-b1c1-6da24bd94caf" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="919" height="255" alt="Screenshot 2025-08-26 111126" src="https://github.com/user-attachments/assets/5759d4d5-d958-4329-aad1-aa5d2a24deba" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="941" height="257" alt="Screenshot 2025-08-26 111210" src="https://github.com/user-attachments/assets/66ebebe3-3f59-4719-a3e8-2d1e65e06ed5" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="963" height="257" alt="Screenshot 2025-08-26 111248" src="https://github.com/user-attachments/assets/d21638d3-818d-4bd8-a1ca-d135940095f0" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="859" height="181" alt="Screenshot 2025-08-26 111312" src="https://github.com/user-attachments/assets/2c6fcd42-60c9-431e-94a2-486eb0460334" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="911" height="119" alt="Screenshot 2025-08-26 111333" src="https://github.com/user-attachments/assets/477f0f72-ded9-427b-98d0-461dd9206961" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="971" height="92" alt="Screenshot 2025-08-26 111402" src="https://github.com/user-attachments/assets/2bdb2c3c-41c1-4931-9e1a-f0c60f33fcb4" />



seq 10 
## OUTPUT
<img width="615" height="310" alt="Screenshot 2025-08-26 111425" src="https://github.com/user-attachments/assets/969ec637-f090-4534-bf26-18b0e7172379" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="829" height="118" alt="Screenshot 2025-08-26 111455" src="https://github.com/user-attachments/assets/ddf7beb7-f2c6-40a2-9fe9-ce4ba190af5f" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="850" height="116" alt="Screenshot 2025-08-26 111522" src="https://github.com/user-attachments/assets/2b78a2bf-fea1-4b07-8dd3-5e14e34fe872" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="835" height="141" alt="Screenshot 2025-08-26 111550" src="https://github.com/user-attachments/assets/35c9c387-d15d-4803-a7ba-d42700b080e2" />



seq 2 | sed '2i hello'
## OUTPUT
<img width="840" height="115" alt="Screenshot 2025-08-26 111614" src="https://github.com/user-attachments/assets/c522dbf1-b0e4-4fb8-8859-ab7c00e5f4f7" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="872" height="111" alt="Screenshot 2025-08-26 111635" src="https://github.com/user-attachments/assets/286907e7-93a2-48f6-87c0-c6401e857521" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="930" height="117" alt="Screenshot 2025-08-26 112250" src="https://github.com/user-attachments/assets/049ecc89-c121-47ed-9071-85c15f9c836c" />



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT
<img width="932" height="121" alt="Screenshot 2025-08-26 112320" src="https://github.com/user-attachments/assets/fb2dc4ac-acb0-44f1-a343-6eee444c2297" />


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

<img width="687" height="176" alt="Screenshot 2025-08-26 112432" src="https://github.com/user-attachments/assets/ba91b9b6-6660-4908-940b-dd9e205359ed" />

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
<img width="681" height="173" alt="Screenshot 2025-08-26 112531" src="https://github.com/user-attachments/assets/4a18f632-47d5-4a18-b507-20f31134ffc9" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="1027" height="257" alt="Screenshot 2025-08-26 112603" src="https://github.com/user-attachments/assets/4414e57f-4523-4f5e-9be0-9a1f5666a3ff" />

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
<img width="905" height="114" alt="Screenshot 2025-08-26 112745" src="https://github.com/user-attachments/assets/593d42d4-4fa8-4cee-bd6c-94f4e350e701" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="1067" height="113" alt="Screenshot 2025-08-26 112810" src="https://github.com/user-attachments/assets/9aa29f9b-0dae-46de-98ac-61dc02bfe50f" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="1731" height="985" alt="Screenshot 2025-08-26 112858" src="https://github.com/user-attachments/assets/ee226710-580c-47ab-9430-3fdc62e4590f" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1919" height="1039" alt="Screenshot 2025-08-26 114540" src="https://github.com/user-attachments/assets/00ebb607-4009-4f0d-8447-469de01b2589" />


tar -xvf backup.tar
## OUTPUT
<img width="1858" height="1007" alt="Screenshot 2025-08-26 114611" src="https://github.com/user-attachments/assets/62e57ad4-e0b0-43ec-9352-66f6336030e4" />

gzip backup.tar

ls .gz
## OUTPUT
<img width="812" height="61" alt="Screenshot 2025-08-26 115048" src="https://github.com/user-attachments/assets/3bb9ee0f-09e6-45f7-b96b-ff09d32a0279" />
 
gunzip backup.tar.gz
## OUTPUT
<img width="961" height="63" alt="Screenshot 2025-08-26 115105" src="https://github.com/user-attachments/assets/cbcd41a1-1a13-4627-a715-83415185a961" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="1187" height="203" alt="image" src="https://github.com/user-attachments/assets/e0f9b9e2-e6e8-42ef-8ebc-f8996eedcc05" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="778" height="116" alt="image" src="https://github.com/user-attachments/assets/654d12cd-301c-45a9-bdfc-1c45bd954e08" />


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
<img width="948" height="475" alt="image" src="https://github.com/user-attachments/assets/351841d0-7e80-4098-b685-72165313ca7a" />

 
ls file1
## OUTPUT
<img width="658" height="60" alt="image" src="https://github.com/user-attachments/assets/2178f54d-6dbd-45fb-8681-46cec4fc8da2" />

echo $?
## OUTPUT 
<img width="627" height="62" alt="image" src="https://github.com/user-attachments/assets/f30a174d-d093-4c86-89fb-d8f3ae6b8f35" />


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
<img width="627" height="58" alt="image" src="https://github.com/user-attachments/assets/e2a4ffdf-606e-47f7-89cd-e8498eed4794" />
 
abcd
 
echo $?
 ## OUTPUT
<img width="621" height="121" alt="image" src="https://github.com/user-attachments/assets/f1c88beb-9724-4540-9e8a-d525acca2bdd" />


 
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
<img width="764" height="281" alt="image" src="https://github.com/user-attachments/assets/0e7eb03f-fa79-4e3d-bad7-368428fbfcfc" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="966" height="63" alt="image" src="https://github.com/user-attachments/assets/306fa7af-0bd3-49d4-a6e7-57bda38681ee" />


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
<img width="853" height="256" alt="image" src="https://github.com/user-attachments/assets/f755db70-ebf3-4611-8a62-d8d1026f6e7e" />

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
<img width="976" height="598" alt="image" src="https://github.com/user-attachments/assets/f9255e70-5013-417b-ae24-9d7be7d5527b" />



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
<img width="802" height="59" alt="image" src="https://github.com/user-attachments/assets/b9005ff3-1a82-4f57-930a-58c48e7a3923" />

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
<img width="832" height="60" alt="image" src="https://github.com/user-attachments/assets/d28d6d3f-7da8-42f2-bf36-9277f47470ff" />

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

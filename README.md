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

<img width="910" height="184" alt="image" src="https://github.com/user-attachments/assets/88ff7cca-ec25-4657-af00-2c5d1681e52b" />


cat < file2
## OUTPUT
<img width="893" height="202" alt="image" src="https://github.com/user-attachments/assets/e9ea202c-ea2b-43ad-a78d-5868eb57be86" />


# Comparing Files
cmp file1 file2
## OUTPUT
 d<img width="883" height="76" alt="image" src="https://github.com/user-attachments/assets/6467d269-2799-48a2-82e6-a95fab3d5503" />

comm file1 file2
 ## OUTPUT
<img width="792" height="227" alt="image" src="https://github.com/user-attachments/assets/7506f4dd-a270-4275-a837-132aa7723335" />


 
diff file1 file2
## OUTPUT
<img width="823" height="276" alt="image" src="https://github.com/user-attachments/assets/79b3e596-bb2f-42b6-bc08-a01d7faddde0" />


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
<img width="780" height="124" alt="image" src="https://github.com/user-attachments/assets/6d83e4f0-cde4-4a91-b97a-b157d3c71f13" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="833" height="150" alt="image" src="https://github.com/user-attachments/assets/1cd4cd76-8052-401e-a6b4-4c811605b26f" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="685" height="152" alt="image" src="https://github.com/user-attachments/assets/8c81dca3-6ef2-4282-b170-c22c04d0c368" />


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
<img width="787" height="78" alt="image" src="https://github.com/user-attachments/assets/e69f8fc6-15a1-4712-8f8b-76d48cc95716" />



grep hello newfile 
## OUTPUT
<img width="760" height="81" alt="image" src="https://github.com/user-attachments/assets/4f0d33c0-7243-433e-bc9c-500cf8a4e5aa" />




grep -v hello newfile 
## OUTPUT
<img width="736" height="105" alt="image" src="https://github.com/user-attachments/assets/2b712892-9554-4f29-961c-1faec3b1c27b" />



cat newfile | grep -i "hello"
## OUTPUT

<img width="743" height="103" alt="image" src="https://github.com/user-attachments/assets/e662f5c9-e941-4f7e-84b2-8e7e3ad877fb" />



cat newfile | grep -i -c "hello"
## OUTPUT
<img width="772" height="76" alt="image" src="https://github.com/user-attachments/assets/c9546098-664a-4e29-a3ea-1b01d8574b3a" />




grep -R ubuntu /etc
## OUTPUT

<img width="1920" height="983" alt="VirtualBox_Parrot Security 6 0_26_04_2026_22_29_40" src="https://github.com/user-attachments/assets/8aa87190-2e02-431b-ac6c-032f513308e4" />


grep -w -n world newfile   
## OUTPUT
<img width="805" height="109" alt="image" src="https://github.com/user-attachments/assets/06811e32-260a-414b-8a59-75065f7e3981" />


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
<img width="737" height="105" alt="image" src="https://github.com/user-attachments/assets/058285f9-41d1-4ca9-a2a0-a94a062c4306" />



egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="740" height="99" alt="image" src="https://github.com/user-attachments/assets/9b6b410f-185c-49a2-8d9f-4834f4a76889" />



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="809" height="104" alt="image" src="https://github.com/user-attachments/assets/85d6d09a-59e6-44e9-9b4f-cf58865fc007" />




egrep '(^hello)' newfile 
## OUTPUT
<img width="794" height="79" alt="image" src="https://github.com/user-attachments/assets/64d8d4c9-a198-437b-992d-9dee7291cc5e" />



egrep '(world$)' newfile 
## OUTPUT

<img width="741" height="101" alt="image" src="https://github.com/user-attachments/assets/3db7d4c8-998f-4ca0-be16-daa2e759924c" />



egrep '(World$)' newfile 
## OUTPUT
<img width="719" height="79" alt="image" src="https://github.com/user-attachments/assets/0229830d-c0ad-4ce4-8a09-730cdb441b04" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="770" height="107" alt="image" src="https://github.com/user-attachments/assets/fb3ae95f-dea0-40ed-99a5-f08d374f9800" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="740" height="77" alt="image" src="https://github.com/user-attachments/assets/cdcc5285-f004-4e6d-8349-9c6ddbbc4d1c" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="661" height="79" alt="image" src="https://github.com/user-attachments/assets/efb5a164-0a6b-4071-80ee-fdbb991a18f5" />


egrep 'Linux.*World' newfile 
## OUTPUT
<img width="741" height="74" alt="image" src="https://github.com/user-attachments/assets/3f25f20c-9ec2-44ff-a7e5-38a390f5ce01" />


egrep l{2} newfile
## OUTPUT
<img width="807" height="107" alt="image" src="https://github.com/user-attachments/assets/e9359b63-8ca2-4d09-85dc-d3ecd5fc386c" />



egrep 's{1,2}' newfile
## OUTPUT 
<img width="769" height="133" alt="image" src="https://github.com/user-attachments/assets/094648c0-4d95-416b-a0a1-3c65c3afbaec" />


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
<img width="782" height="78" alt="image" src="https://github.com/user-attachments/assets/7074bbac-984f-4580-aaab-620777087eca" />



sed -n -e '$p' file23
## OUTPUT
<img width="709" height="77" alt="image" src="https://github.com/user-attachments/assets/0acfe4df-af48-4403-b6a1-a4ba9980b04d" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="860" height="281" alt="image" src="https://github.com/user-attachments/assets/9bb5550f-f841-4f6a-93e9-688e5fb80435" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="742" height="279" alt="image" src="https://github.com/user-attachments/assets/388a827d-0441-4251-b715-1cfc538f0d49" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="901" height="274" alt="image" src="https://github.com/user-attachments/assets/319f2400-e165-445a-aac4-e2b905b93175" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="719" height="179" alt="image" src="https://github.com/user-attachments/assets/c3a45481-bda0-4801-85a1-44c1853768fd" />



sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="703" height="124" alt="image" src="https://github.com/user-attachments/assets/c3dceb2d-833f-4f69-a1ff-3d065323935f" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="731" height="100" alt="image" src="https://github.com/user-attachments/assets/522bbf9f-4eef-4f94-be36-984ded9773b8" />



seq 10 
## OUTPUT
<img width="891" height="305" alt="image" src="https://github.com/user-attachments/assets/a01e434c-d240-4470-b09e-b7d71f390c91" />



seq 10 | sed -n '4,6p'
## OUTPUT
<img width="704" height="136" alt="image" src="https://github.com/user-attachments/assets/f1ad766f-4755-4ced-bd87-44141508c627" />



seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="756" height="126" alt="image" src="https://github.com/user-attachments/assets/4b9d89ed-dbbe-46a7-96ce-2beceb9375c2" />



seq 3 | sed '2a hello'
## OUTPUT
<img width="759" height="151" alt="image" src="https://github.com/user-attachments/assets/6800008c-84b5-4b58-8769-eaf0c442673a" />




seq 2 | sed '2i hello'
## OUTPUT
<img width="693" height="130" alt="image" src="https://github.com/user-attachments/assets/2d08c967-e4bc-490e-93b3-f1dc692a1730" />


seq 10 | sed '2,9c hello'
## OUTPUT
<img width="671" height="124" alt="image" src="https://github.com/user-attachments/assets/7214fda2-982a-4ea0-a3db-697f61d9dbc6" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="746" height="128" alt="image" src="https://github.com/user-attachments/assets/1c45cf69-af30-4d64-aac4-ee47904f98d4" />



sed -n '2,4{s/$/*/;p}' file23
<img width="799" height="132" alt="image" src="https://github.com/user-attachments/assets/ea4fa368-026c-42a2-bfa4-3311d20a49c8" />


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
<img width="717" height="179" alt="image" src="https://github.com/user-attachments/assets/c6addeaa-899a-4465-bf70-1841e917c5be" />


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
<img width="727" height="178" alt="image" src="https://github.com/user-attachments/assets/94400382-847c-4680-833a-1db925cd2238" />



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
<img width="790" height="283" alt="image" src="https://github.com/user-attachments/assets/f349efc7-b464-4e6a-93e9-68121e4ea68a" />


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
<img width="693" height="122" alt="image" src="https://github.com/user-attachments/assets/b4598546-b0be-4c8d-8894-9e1dbe5ad2d7" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="700" height="124" alt="image" src="https://github.com/user-attachments/assets/e62fa02a-4a46-4f86-91bb-55b24b30a248" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="828" height="244" alt="image" src="https://github.com/user-attachments/assets/45fbf62e-0fed-40da-bfb3-4bb8fa1f72f9" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="878" height="257" alt="image" src="https://github.com/user-attachments/assets/5871eb15-6f1b-4589-9f43-20b234e7ea1c" />

tar -xvf backup.tar
## OUTPUT
<img width="792" height="251" alt="image" src="https://github.com/user-attachments/assets/0271fa83-0f17-472f-8de2-6994301e7b29" />

gzip backup.tar

ls *.gz
## OUTPUT
 <img width="831" height="83" alt="image" src="https://github.com/user-attachments/assets/625a65d2-8e30-4875-8c6f-57a08d40c73f" />

gunzip backup.tar.gz
## OUTPUT
<img width="893" height="136" alt="image" src="https://github.com/user-attachments/assets/6de2d5f7-09bf-4fd8-ba51-be3f431f3368" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="702" height="185" alt="image" src="https://github.com/user-attachments/assets/2b8bace5-152b-475a-b27b-98893ca3e35d" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="731" height="133" alt="image" src="https://github.com/user-attachments/assets/a1ebb622-ad9a-47de-a5b9-96bf015d6770" />


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
<img width="924" height="707" alt="image" src="https://github.com/user-attachments/assets/3de611cf-5394-4f35-abe1-e9f4443f62ec" />

 
ls file1
## OUTPUT
<img width="735" height="75" alt="image" src="https://github.com/user-attachments/assets/c5bdd672-15ea-4cf2-afe6-b8734ec018ce" />

echo $?
## OUTPUT 
<img width="693" height="76" alt="image" src="https://github.com/user-attachments/assets/ba5a1e28-5ea9-4140-8a89-2db97d853c58" />

./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 <img width="798" height="81" alt="image" src="https://github.com/user-attachments/assets/7efa68a2-469b-4351-a6bd-7831cb948f53" />

abcd
 
echo $?
 ## OUTPUT
<img width="798" height="81" alt="image" src="https://github.com/user-attachments/assets/d3aa9d1c-19fd-4525-8cc5-602be6e173e4" />


 
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
<img width="827" height="273" alt="image" src="https://github.com/user-attachments/assets/ddde0e2d-92d4-44a2-9002-7d71c63c2d81" />



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="819" height="108" alt="image" src="https://github.com/user-attachments/assets/3e35ca94-407d-4463-9663-c89c67ae8066" />


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
## OUTPUT
<img width="839" height="229" alt="image" src="https://github.com/user-attachments/assets/e5c2a5f2-e40f-4f91-8b69-ea13da73c6e6" />

./psswdperm.sh
## OUTPUT
<img width="778" height="152" alt="image" src="https://github.com/user-attachments/assets/4ef6c1a6-1afd-41d4-8e0c-450754981711" />


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
<img width="871" height="161" alt="image" src="https://github.com/user-attachments/assets/a5a48e0c-df33-4416-95a7-239a96a19219" />



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
<img width="885" height="101" alt="image" src="https://github.com/user-attachments/assets/3c9e67a8-4ba6-4e84-a1f3-e189ced3b773" />

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
<img width="880" height="127" alt="image" src="https://github.com/user-attachments/assets/2d9d47c5-5049-4c8a-9560-f8cf354a0357" />

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
<img width="893" height="97" alt="image" src="https://github.com/user-attachments/assets/571dc978-39a2-4de7-b49c-1214ce5899c5" />


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
<img width="851" height="82" alt="image" src="https://github.com/user-attachments/assets/bfe38e41-4511-48a0-a297-249b63e62e3a" />

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
## OUTPUT
<img width="852" height="109" alt="image" src="https://github.com/user-attachments/assets/771965d1-6255-4cc4-883b-96cd0fe7053b" />

 
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
 ## OUTPUT
 <img width="853" height="305" alt="image" src="https://github.com/user-attachments/assets/f73251a0-5252-476b-80aa-7649824cd0df" />

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
 ## OUTPUT
 <img width="731" height="153" alt="image" src="https://github.com/user-attachments/assets/08fdd057-6eac-48fe-8298-3b04d0da0e85" />

 
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
 ## OUTPUT
 <img width="801" height="206" alt="image" src="https://github.com/user-attachments/assets/a2b7be9d-9b6d-4e77-bf62-b4326bc389a0" />

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
 <img width="870" height="126" alt="image" src="https://github.com/user-attachments/assets/f8ca6186-08d4-4b9d-b022-724cb8603c62" />


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
## OUTPUT 
<img width="757" height="198" alt="image" src="https://github.com/user-attachments/assets/f07e30b9-28e1-4b88-86e6-5bf9b1e470bb" />

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
/forinfile.sh
## OUTPUT
<img width="785" height="77" alt="image" src="https://github.com/user-attachments/assets/c6afe116-bcdf-4181-81fe-3b3cde264189" />

$ cat cities
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam

## OUTPUT
<img width="785" height="77" alt="image" src="https://github.com/user-attachments/assets/c6afe116-bcdf-4181-81fe-3b3cde264189" />

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
<img width="780" height="179" alt="image" src="https://github.com/user-attachments/assets/0a374afc-2532-4145-a771-6cf6b93ca94d" />

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
<img width="773" height="183" alt="image" src="https://github.com/user-attachments/assets/50f49055-200f-40de-95d1-ebf75adb4fb5" />

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
<img width="887" height="354" alt="image" src="https://github.com/user-attachments/assets/0d95a8d4-df62-4c44-b381-2131e146b86b" />

 
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
 <img width="779" height="125" alt="image" src="https://github.com/user-attachments/assets/43de4ce6-f125-46a6-9d32-4acd2f2a8231" />

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
 
$  ./forcontinue.sh
## OUTPUT
<img width="830" height="174" alt="image" src="https://github.com/user-attachments/assets/685d1402-9040-4ec3-8d93-7ebdafc980e4" />

 
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
<img width="799" height="104" alt="image" src="https://github.com/user-attachments/assets/68af323e-9c59-401b-88a0-92762ed9e806" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 
$ ./exread1.sh 
## OUTPUT
<img width="792" height="103" alt="image" src="https://github.com/user-attachments/assets/5b644c37-5dec-4e2c-a12e-7058f9c75f53" />




 
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
## OUTPUT
 <img width="723" height="74" alt="image" src="https://github.com/user-attachments/assets/e3351274-73eb-4351-8922-d43a52eba75a" />

 ./funcex.sh 1 2
## OUTPUT
<img width="786" height="78" alt="image" src="https://github.com/user-attachments/assets/347ebb4b-1c1e-4e13-841f-aae2ae590768" />
 
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

<img width="773" height="127" alt="image" src="https://github.com/user-attachments/assets/e5e8c693-47d5-4f05-bdf6-e34435113213" />

 
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


<img width="773" height="127" alt="image" src="https://github.com/user-attachments/assets/0335d5aa-ae08-4722-9ac6-b531a4867028" />

 
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
 
 <img width="902" height="404" alt="image" src="https://github.com/user-attachments/assets/04481b14-d813-49a1-8b91-d39d95ed0271" />

 
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
 <img width="815" height="383" alt="image" src="https://github.com/user-attachments/assets/3549e5dd-7453-46cb-a4b1-caf73724c2ce" />

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
chmod 777 palindrome.sh
./palindrome.sh

## OUTPUT 
<img width="838" height="303" alt="image" src="https://github.com/user-attachments/assets/533d4f23-a24b-4e85-9a6c-e34789a0cdf0" />


# RESULT:
The Commands are executed successfully.

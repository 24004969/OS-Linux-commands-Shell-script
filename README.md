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

<img width="624" height="159" alt="image" src="https://github.com/user-attachments/assets/926b2c68-ee58-4da6-b206-12ab34639bab" />


cat < file2
## OUTPUT
<img width="624" height="176" alt="image" src="https://github.com/user-attachments/assets/e7f32fc0-7bcc-4e8b-abca-ec520c4ebe4a" />


# Comparing Files
cmp file1 file2
## OUTPUT
<img width="625" height="79" alt="image" src="https://github.com/user-attachments/assets/2b325d3e-095a-450f-bd6d-441fea80e9c6" />


comm file1 file2
 ## OUTPUT
<img width="661" height="230" alt="image" src="https://github.com/user-attachments/assets/b2d6b6e7-82e7-414d-be44-de2d592aae5b" />

 
diff file1 file2
## OUTPUT
<img width="632" height="279" alt="image" src="https://github.com/user-attachments/assets/7a5f0f04-3676-468c-addd-acd83a4a71cb" />


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
<img width="609" height="95" alt="image" src="https://github.com/user-attachments/assets/4880b179-2f78-4c96-aaac-b4fcfbd04f53" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="612" height="120" alt="image" src="https://github.com/user-attachments/assets/9be9ead1-91ae-4666-8b8e-d1ca48b033eb" />



cut -d "|" -f 2 file22
## OUTPUT

<img width="601" height="127" alt="image" src="https://github.com/user-attachments/assets/04fb2625-e450-415b-aabb-96d5c1fe47d0" />


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
<img width="614" height="84" alt="image" src="https://github.com/user-attachments/assets/4f54d74a-09e6-4bf6-b150-f8394bf4270a" />



grep hello newfile 
## OUTPUT

<img width="610" height="79" alt="image" src="https://github.com/user-attachments/assets/66a03241-c301-43c4-bfaf-edf1f07efd92" />



grep -v hello newfile 
## OUTPUT

<img width="610" height="79" alt="image" src="https://github.com/user-attachments/assets/2e7ac1ae-1f99-42f2-8123-4421fe3dfbe5" />


cat newfile | grep -i "hello"
## OUTPUT

<img width="626" height="104" alt="image" src="https://github.com/user-attachments/assets/de3a92ee-5078-4ed3-aeb3-ec28c84a97a7" />



cat newfile | grep -i -c "hello"
## OUTPUT

<img width="614" height="85" alt="image" src="https://github.com/user-attachments/assets/e258dadd-8f41-4a68-826e-bbc7d831c0d0" />



grep -R ubuntu /etc
## OUTPUT

<img width="656" height="83" alt="image" src="https://github.com/user-attachments/assets/64584f6b-73e1-4301-99ea-b90b4bd0e450" />


grep -w -n world newfile   
## OUTPUT

<img width="649" height="92" alt="image" src="https://github.com/user-attachments/assets/6bda42ad-ec03-40a7-ac00-ea8039acfe05" />


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
<img width="617" height="109" alt="image" src="https://github.com/user-attachments/assets/e348def8-7b9e-4954-a703-395fd941a2df" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="672" height="100" alt="image" src="https://github.com/user-attachments/assets/8ad8d0f5-30b0-4569-a54e-0ad561c952b4" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="615" height="107" alt="image" src="https://github.com/user-attachments/assets/50e74252-baef-4640-a7df-95578c419868" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="615" height="75" alt="image" src="https://github.com/user-attachments/assets/0fcf55c0-f12b-4cab-8911-e878711c4d99" />


egrep '(world$)' newfile 
## OUTPUT

<img width="626" height="102" alt="image" src="https://github.com/user-attachments/assets/d5242ec7-cb75-4d9d-bee0-380746cb8414" />


egrep '(World$)' newfile 
## OUTPUT

<img width="618" height="78" alt="image" src="https://github.com/user-attachments/assets/ae301d25-01ee-4136-b16f-fe555fdff1c8" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="626" height="133" alt="image" src="https://github.com/user-attachments/assets/d2cd6076-7b6d-4c4c-9c9d-3bc70804a40c" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="628" height="83" alt="image" src="https://github.com/user-attachments/assets/2b9239d6-eabe-4cb5-90f1-c8d3d52e1105" />

egrep 'Linux.*world' newfile 
## OUTPUT

<img width="625" height="73" alt="image" src="https://github.com/user-attachments/assets/4dead726-cd6a-4cf1-9aa6-0afe397c6e4d" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="636" height="76" alt="image" src="https://github.com/user-attachments/assets/dd559fa4-f7e5-4859-867b-acd602f1f166" />


egrep l{2} newfile
## OUTPUT
<img width="631" height="112" alt="image" src="https://github.com/user-attachments/assets/e9f037e3-74b6-4f71-a8c0-2abd30bc261c" />



egrep 's{1,2}' newfile
## OUTPUT 

<img width="650" height="124" alt="image" src="https://github.com/user-attachments/assets/a302302f-c063-4138-9879-ffca492a58fb" />


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

<img width="638" height="83" alt="image" src="https://github.com/user-attachments/assets/6b9d61f1-25c8-4b87-90bb-dd4964c94fbc" />


sed -n -e '$p' file23
## OUTPUT

<img width="639" height="84" alt="image" src="https://github.com/user-attachments/assets/645c6bbb-f9ab-4f22-9eba-7ef3c109ebe4" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="626" height="246" alt="image" src="https://github.com/user-attachments/assets/65a160c5-116e-4e02-86bb-98ee8a14cb73" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="666" height="248" alt="image" src="https://github.com/user-attachments/assets/97bdc3d6-ec02-46d1-b8a1-3e1e83a99966" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="659" height="256" alt="image" src="https://github.com/user-attachments/assets/ec286ca6-ee73-4f38-8d5d-9f1951042714" />


sed -n -e '1,5p' file23
## OUTPUT
<img width="628" height="185" alt="image" src="https://github.com/user-attachments/assets/10ecb401-352c-48f4-95ee-16c508535ed9" />

sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="622" height="132" alt="image" src="https://github.com/user-attachments/assets/c7eb18ce-75b3-4d1a-ae6b-89c4087e2957" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="628" height="107" alt="image" src="https://github.com/user-attachments/assets/78679823-bc0e-46e1-92cc-e277d94a23c0" />


seq 10 
## OUTPUT

<img width="655" height="304" alt="image" src="https://github.com/user-attachments/assets/efd4e1ec-0c3d-4afe-9609-cc77925afac3" />


seq 10 | sed -n '4,6p'
## OUTPUT


<img width="631" height="134" alt="image" src="https://github.com/user-attachments/assets/4faf639c-8f83-4554-ba29-9e067d5ba33a" />

seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="673" height="126" alt="image" src="https://github.com/user-attachments/assets/ddba0a96-c65c-49ff-9e3d-b3b1c05373c0" />


seq 3 | sed '2a hello'
## OUTPUT

<img width="658" height="161" alt="image" src="https://github.com/user-attachments/assets/8eb4d45b-84d1-42e6-89f7-193a92454d60" />


seq 2 | sed '2i hello'
## OUTPUT

<img width="622" height="139" alt="image" src="https://github.com/user-attachments/assets/d76beac0-2ed7-48a0-b7e5-e09c03716bf7" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="669" height="120" alt="image" src="https://github.com/user-attachments/assets/338b5f4e-0d9d-4e68-9e59-44612cf64798" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="639" height="140" alt="image" src="https://github.com/user-attachments/assets/22047ae7-1ab0-48c2-9ed3-08f33792be80" />


sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

<img width="630" height="132" alt="image" src="https://github.com/user-attachments/assets/3c4499f8-8510-4c5a-869e-7ce10b657823" />


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

<img width="664" height="187" alt="image" src="https://github.com/user-attachments/assets/aabeea89-f694-4e1e-9bcd-222a596ca9b5" />


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

<img width="638" height="205" alt="image" src="https://github.com/user-attachments/assets/cec41441-cfd2-4601-9cb8-6ec2653a5186" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="629" height="255" alt="image" src="https://github.com/user-attachments/assets/27d1f482-7216-4b14-aacb-a395a3fcbb2c" />


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

<img width="627" height="125" alt="image" src="https://github.com/user-attachments/assets/207e077f-ce70-463c-88e1-bab029148b4f" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="627" height="123" alt="image" src="https://github.com/user-attachments/assets/5a99d5aa-b028-4e68-8241-8d34a42fa0b3" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="633" height="550" alt="image" src="https://github.com/user-attachments/assets/de5ad016-7dd7-4da6-8692-7b492ce1ad1e" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT

<img width="738" height="580" alt="image" src="https://github.com/user-attachments/assets/45c9d896-e99c-43b6-8b24-f99f7e0e452e" />


tar -xvf backup.tar
## OUTPUT
<img width="741" height="575" alt="image" src="https://github.com/user-attachments/assets/7b4de7c1-c063-4a11-a5fe-3ada42c122ca" />


gzip backup.tar

ls .gz
## OUTPUT
 
<img width="782" height="62" alt="image" src="https://github.com/user-attachments/assets/aec31a6d-a160-49f5-aff6-00d28899670f" />


gunzip backup.tar.gz
## OUTPUT

<img width="782" height="62" alt="image" src="https://github.com/user-attachments/assets/81b8d461-2810-4e74-86a5-0108e679aea1" />


# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘;exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

<img width="605" height="61" alt="image" src="https://github.com/user-attachments/assets/e91765c4-377c-4693-b3be-096377399c65" />


cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

<img width="639" height="157" alt="image" src="https://github.com/user-attachments/assets/29f3177f-221f-496f-8b1c-6c769a431d0a" />

cat < scriptest.sh 
```bash
#!/bin/sh
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
```

cat scriptest.sh 
```bash
#!/bin/sh
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

<img width="688" height="448" alt="image" src="https://github.com/user-attachments/assets/17a6b397-802e-4f39-894a-ca3d49867e12" />


ls file1
## OUTPUT

<img width="657" height="83" alt="image" src="https://github.com/user-attachments/assets/a6428f90-6414-43a5-a2db-d73538c61073" />

echo $?
## OUTPUT 

<img width="657" height="83" alt="image" src="https://github.com/user-attachments/assets/fdbed965-c812-4def-98c8-54781c96f11c" />

./onebash:./one: Permission denied
 
abcd
 
echo $?
 ## OUTPUT

<img width="658" height="158" alt="image" src="https://github.com/user-attachments/assets/16b19999-3769-4ff4-b23b-6f1e822d4b7c" />

 
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
#!/bin/bash
val1=baseball
val2=hockey
if [ $val1 \> $val2 ]
then
echo "$val1 is greater than $val2"
else
echo "$val1 is less than $val2"
fi
```
chmod 755 strcomp.sh 
./strcomp.sh 
## OUTPUT

<img width="689" height="305" alt="image" src="https://github.com/user-attachments/assets/50881866-d265-4f2b-a093-f40eae9b1be1" />


# check file ownership
cat < psswdperm.sh 
```bash
#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
```

cat psswdperm.sh 
```bash
#!/bin/bash
if [ -O /etc/passwd ]
then
echo “You are the owner of the /etc/passwd file”
else
echo “Sorry, you are not the owner of the /etc/passwd file”
fi
 ```
./psswdperm.sh
## OUTPUT

<img width="624" height="76" alt="image" src="https://github.com/user-attachments/assets/84419eee-c892-43f5-a303-c17bf3546337" />


# check if with file location
cat>ifnested.sh 
```bash
#!/bin/bash
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
cat ifnested.sh 
```bash
#!/bin/bash
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

<img width="613" height="134" alt="image" src="https://github.com/user-attachments/assets/17d8ce7c-094d-468a-b979-5cceb547f293" />


# using numeric test comparisons
cat > iftest.sh 
```bash
#!/bin/bash
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


cat iftest.sh 
```bash
#!/bin/bash
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

chmod 755 iftest.sh
 
./iftest.sh 
## OUTPUT

<img width="637" height="104" alt="image" src="https://github.com/user-attachments/assets/268f8a08-168a-4c44-990d-ea13b0d50c62" />


# check if a file
cat > ifnested.sh 
```bash
#!/bin/bash
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

cat ifnested.sh 
```bash
#!/bin/bash
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

<img width="626" height="132" alt="image" src="https://github.com/user-attachments/assets/ab9c670f-2a95-4e32-9d04-46a5929f86f4" />


# looking for a possible value using elif
cat elifcheck.sh 
```bash
#!/bin/bash
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

chmod 755 elifcheck.sh
 
./elifcheck.sh 
## OUTPUT

<img width="637" height="81" alt="image" src="https://github.com/user-attachments/assets/fd7fb3b4-eea3-4789-a680-400e41958fbf" />


# testing compound comparisons
cat> ifcompound.sh 
```bash
#!/bin/bash
if [ -d $HOME ] && [ -w $HOME ]
then
echo "The file exists and you can write to it"
else
echo "I cannot write to the file"
fi
```
chmod 755 ifcompound.sh
./ifcompound.sh 
## OUTPUT

<img width="610" height="78" alt="image" src="https://github.com/user-attachments/assets/cdbfb042-c377-4936-a731-0a4fd171c905" />


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

<img width="623" height="79" alt="image" src="https://github.com/user-attachments/assets/ba2ddb6c-f334-4f54-a334-bcb4eba856fb" />


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
chmod 755 whiletest.sh
 
./whiletest.sh
 ## OUTPUT

<img width="603" height="307" alt="image" src="https://github.com/user-attachments/assets/6d4bf7d4-fb8f-49c0-970d-20209108f908" />

 
cat untiltest.sh 
```bash
#using the until command
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

<img width="621" height="156" alt="image" src="https://github.com/user-attachments/assets/c586be5a-0486-4fbd-924b-8914b06ad8e2" />

cat forin1.sh 
```bash
#!/bin/bash
#basic for command
for test in Alabama Alaska Arizona Arkansas California Colorado
do
echo The next state is $test
done
 ```
 
$ chmod 755 forin1.sh
$ ./forin1.sh
## OUTPUT

<img width="635" height="225" alt="image" src="https://github.com/user-attachments/assets/84945c0a-fd48-43b2-bb1c-7de5e4c5e431" />

 
cat forin2.sh 
```bash
#!/bin/bash
# another example of how not to use the for command
for test in I don't know if this'll work
do
echo “word:$test”
done
 ```
 
$ chmod 755 forin2.sh
 
$ ./forin2.sh 
## OUTPUT


<img width="624" height="157" alt="image" src="https://github.com/user-attachments/assets/e3be67a8-e42a-4551-b4d4-de618b33defc" />


cat forin3.sh 
```bash
#!/bin/bash
# another example of how not to use the for command
for test in I don\'t know if "this'll" work
do
echo "word:$test"
done
```
$ chmod 755 forin3.sh
$ ./forin3.sh 
## OUTPUT


<img width="633" height="232" alt="image" src="https://github.com/user-attachments/assets/fa4e7222-9727-4c18-8f14-c67a9d349366" />


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

<img width="617" height="201" alt="image" src="https://github.com/user-attachments/assets/58722d5b-e846-4051-a923-65b486af360e" />


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

$ cat > cities
```
Hyderabad
Alampur
Basara
Warangal
Adilabad
Bhadrachalam
Khammam
```
./forinfile.sh
## OUTPUT


<img width="632" height="92" alt="image" src="https://github.com/user-attachments/assets/ebc2c909-5f9c-48da-bc05-9a0c7277472b" />


cat forctype.sh 
```bash
#!/bin/bash
# testing the C-style for loop
for (( i=1; i <= 5; i++ ))
do
echo "The value of i is $i"
done
```
$ chmod 755 forctype.sh
$ ./forctype.sh 
## OUTPUT


<img width="640" height="181" alt="image" src="https://github.com/user-attachments/assets/1221bbec-8434-49f0-93b8-90adc8a06527" />


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

<img width="624" height="177" alt="image" src="https://github.com/user-attachments/assets/1ad994d3-15eb-4230-8633-b262b094f805" />


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

<img width="615" height="135" alt="image" src="https://github.com/user-attachments/assets/7016721e-5f15-4453-a298-73ab2a464277" />


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

<img width="619" height="156" alt="image" src="https://github.com/user-attachments/assets/fece84b6-9f02-4296-ad2e-6731ad70888a" />

cat > forcontinue.sh 
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
 
<img width="624" height="108" alt="image" src="https://github.com/user-attachments/assets/70452f37-5fa8-4647-8125-9205f15c40de" />


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

![Alt text](<img/. exread.sh.png>)

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

<img width="637" height="106" alt="image" src="https://github.com/user-attachments/assets/b4daa358-6fcb-4f27-a0b3-8c5549c71dbf" />


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
$ chmod 755 funcex.sh
$ ./funcex.sh 

## OUTPUT
 
<img width="613" height="83" alt="image" src="https://github.com/user-attachments/assets/11af6a7e-87aa-4758-8348-3cd26043bf45" />

 
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

<img width="633" height="129" alt="image" src="https://github.com/user-attachments/assets/0b11a257-b7a3-458d-8566-fe49dab9a508" />

 
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
$ chmod 777 argshift1.sh

$ ./argshift1.sh 1 2 3
## OUTPUT

<img width="610" height="133" alt="image" src="https://github.com/user-attachments/assets/ca0f5df5-18ae-4833-9cfd-8bd526c00889" />

 
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
 
 <img width="642" height="410" alt="image" src="https://github.com/user-attachments/assets/e8564f4b-cd77-47f0-8aee-60a89850bc88" />

 
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

<img width="611" height="375" alt="image" src="https://github.com/user-attachments/assets/e80fd51e-3f07-4843-baa0-8f1673becaef" />

 
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
$chmod 755 palindrome.sh

$./palindrome.sh
## OUTPUT 

<img width="609" height="135" alt="image" src="https://github.com/user-attachments/assets/4d772654-add9-4f25-b6e9-f5de3bd513a0" />


# RESULT:
The Commands are executed successfully.

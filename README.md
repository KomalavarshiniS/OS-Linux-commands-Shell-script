<img width="775" height="38" alt="image" src="https://github.com/user-attachments/assets/aec705d7-453c-4a9b-b500-c7c8e1320766" /># OS-Linux-commands-Shell-scripting
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
![alt text](<WhatsApp Image 2025-08-29 at 17.59.21_880e366e.jpg>)


cat < file2
## OUTPUT
![alt text](<WhatsApp Image 2025-08-29 at 17.59.22_05f9f745.jpg>)

# Comparing Files
cmp file1 file2
## OUTPUT
![alt text](<WhatsApp Image 2025-08-29 at 17.59.22_28216bae.jpg>)
 

comm file1 file2
 ## OUTPUT

 ![alt text](<WhatsApp Image 2025-08-29 at 17.59.23_dc30f9d1.jpg>)
diff file1 file2
## OUTPUT

![alt text](<WhatsApp Image 2025-08-29 at 18.02.07_5b0d0e94.jpg>)
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

![alt text](<WhatsApp Image 2025-08-29 at 18.01.44_7ebc7ca4.jpg>)


cut -d "|" -f 1 file22
## OUTPUT


![alt text](<WhatsApp Image 2025-08-29 at 18.01.44_f6102fcc.jpg>)
cut -d "|" -f 2 file22
## OUTPUT
![alt text](<WhatsApp Image 2025-08-29 at 18.01.45_616e6b7b.jpg>)

cat < newfile 
```
Hello world
hello world
^d
```
cat > newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT

![alt text](<WhatsApp Image 2025-08-29 at 18.01.45_cf740200.jpg>)

grep hello newfile 
## OUTPUT




grep -v hello newfile 
## OUTPUT

![alt text](<WhatsApp Image 2025-08-29 at 18.01.45_a5dab47e.jpg>)

cat newfile | grep -i "hello"
## OUTPUT

![alt text](<WhatsApp Image 2025-08-29 at 18.01.45_109d37ae.jpg>)


cat newfile | grep -i -c "hello"
## OUTPUT

![alt text](<WhatsApp Image 2025-08-29 at 18.01.45_2c04ee31.jpg>)


grep -R ubuntu /etc
## OUTPUT

![alt text](<WhatsApp Image 2025-08-24 at 18.52.31_1ae8d506.jpg>)

grep -w -n world newfile   
## OUTPUT

![alt text](<WhatsApp Image 2025-08-29 at 18.35.04_5f6b5f94.jpg>)
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

![alt text](<WhatsApp Image 2025-08-29 at 18.35.05_8bc31089.jpg>)

egrep -w '(H|h)ello' newfile 
## OUTPUT



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT


![alt text](<WhatsApp Image 2025-08-29 at 18.35.05_33925dca.jpg>)

egrep '(^hello)' newfile 
## OUTPUT

![alt text](<WhatsApp Image 2025-08-29 at 18.35.06_5ed7a30a.jpg>)

egrep '(world$)' newfile 
## OUTPUT

![alt text](<WhatsApp Image 2025-08-29 at 18.35.06_24cbe0d8.jpg>)

egrep '(World$)' newfile 
## OUTPUT
![alt text](<WhatsApp Image 2025-08-29 at 18.35.05_8a36f67c.jpg>)

egrep '((W|w)orld$)' newfile 
## OUTPUT

![alt text](<WhatsApp Image 2025-08-29 at 18.35.07_10b578ec.jpg>)

egrep '[1-9]' newfile 
## OUTPUT
![alt text](<WhatsApp Image 2025-08-29 at 18.35.07_65cd7936.jpg>)


egrep 'Linux.*world' newfile 
## OUTPUT
![alt text](<WhatsApp Image 2025-08-29 at 18.35.07_935604f8.jpg>)

egrep 'Linux.*World' newfile 
## OUTPUT

![alt text](<WhatsApp Image 2025-08-29 at 18.35.07_3a4b7077.jpg>)
egrep l{2} newfile
## OUTPUT

![alt text](<WhatsApp Image 2025-08-29 at 18.35.07_76f92a7d.jpg>)

egrep 's{1,2}' newfile
## OUTPUT 
![alt text](<WhatsApp Image 2025-08-29 at 18.35.07_8279da5f.jpg>)

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

![alt text](<WhatsApp Image 2025-08-31 at 17.00.44_58e36a77.jpg>)

sed -n -e '$p' file23
## OUTPUT

![alt text](<WhatsApp Image 2025-08-31 at 17.00.44_bb019940.jpg>)

sed  -e 's/Ram/Sita/' file23
## OUTPUT

![alt text](<WhatsApp Image 2025-08-31 at 17.00.44_31109491.jpg>)

sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![alt text](<WhatsApp Image 2025-08-31 at 17.00.44_c4132a39.jpg>)

sed  '/tom/s/5000/6000/' file23
## OUTPUT

![alt text](<WhatsApp Image 2025-08-31 at 17.00.44_82c48264.jpg>)

sed -n -e '1,5p' file23
## OUTPUT

![alt text](<WhatsApp Image 2025-08-31 at 17.00.44_cfdc1b4b.jpg>)

sed -n -e '2,/Joe/p' file23
## OUTPUT

![alt text](<WhatsApp Image 2025-08-31 at 17.00.44_abd62463.jpg>)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![alt text](<WhatsApp Image 2025-08-31 at 17.00.45_10b4550a.jpg>)


seq 10 
## OUTPUT

![alt text](<WhatsApp Image 2025-08-31 at 17.00.45_f748d3db.jpg>)

seq 10 | sed -n '4,6p'
## OUTPUT
![alt text](<WhatsApp Image 2025-08-31 at 17.00.45_3b20aa57.jpg>)


seq 10 | sed -n '2,~4p'
## OUTPUT

![alt text](<WhatsApp Image 2025-08-31 at 17.00.45_c7bc53fe.jpg>)

seq 3 | sed '2a hello'
## OUTPUT

![alt text](<WhatsApp Image 2025-08-31 at 17.00.45_4bf5bb56.jpg>)

seq 2 | sed '2i hello'
## OUTPUT
![alt text](<WhatsApp Image 2025-08-31 at 17.00.45_ba6b174a.jpg>)

seq 10 | sed '2,9c hello'
## OUTPUT
![alt text](<WhatsApp Image 2025-08-31 at 17.00.45_9905f812.jpg>)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT


![alt text](<WhatsApp Image 2025-08-31 at 17.00.45_2ef8dc7a.jpg>)
sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![alt text](<WhatsApp Image 2025-08-31 at 17.00.46_4e17911c.jpg>)
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
![alt text](<WhatsApp Image 2025-08-31 at 17.00.46_30e30686.jpg>)

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

![alt text](<WhatsApp Image 2025-08-31 at 17.00.46_09a5961f.jpg>)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![alt text](<WhatsApp Image 2025-08-31 at 17.00.46_66904850.jpg>)
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

![alt text](<WhatsApp Image 2025-08-31 at 17.00.46_dfd4a0f9.jpg>)
 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![alt text](<WhatsApp Image 2025-08-31 at 17.00.46_ae2bda95.jpg>)

#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="479" height="307" alt="image" src="https://github.com/user-attachments/assets/fa48eb18-c2d7-4d5d-880d-ef0e1b39f38f" />

mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="570" height="403" alt="image" src="https://github.com/user-attachments/assets/7364a8d0-d9c8-4e4c-bcf9-44e5b6a5d198" />


tar -xvf backup.tar
## OUTPUT
<img width="972" height="376" alt="image" src="https://github.com/user-attachments/assets/1b756675-9de3-44e8-83a8-ae15fc932af6" />

gzip backup.tar

ls .gz
## OUTPUT
 ![WhatsApp Image 2025-10-19 at 06 37 07_364c98e3](https://github.com/user-attachments/assets/39ba5d63-cf26-4e82-b455-ddf2e072dace)

gunzip backup.tar.gz
## OUTPUT
![WhatsApp Image 2025-10-19 at 06 37 09_6e0fe0cc](https://github.com/user-attachments/assets/48120b85-555a-4458-a3a5-429e19bb2c66)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

 ![WhatsApp Image 2025-10-19 at 06 37 10_2a972517](https://github.com/user-attachments/assets/b86f719a-b8ef-4c7a-8092-088b5e6f849e)

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![WhatsApp Image 2025-10-19 at 06 37 14_48d40709](https://github.com/user-attachments/assets/1ca9a1f7-d615-45fe-a465-87c6e4e0e28c)


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

 ![WhatsApp Image 2025-10-19 at 06 37 22_f3c4d6ea](https://github.com/user-attachments/assets/7b6e6d2e-0699-4810-bd74-911efe842acb)

ls file1
## OUTPUT
![WhatsApp Image 2025-10-19 at 06 37 22_f3c4d6ea](https://github.com/user-attachments/assets/7e368970-3768-4ffa-817b-8b9665cbcac1)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![WhatsApp Image 2025-10-19 at 06 37 22_f3c4d6ea](https://github.com/user-attachments/assets/a4ebe48f-e994-468f-bd88-362c7b968289)

abcd
 
echo $?
 ## OUTPUT

![WhatsApp Image 2025-10-19 at 06 37 22_f3c4d6ea](https://github.com/user-attachments/assets/433ee044-6e46-485a-a5c6-5439f66c4a25)

 
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
![WhatsApp Image 2025-10-19 at 06 37 48_905ca523](https://github.com/user-attachments/assets/6f0a987a-4c87-4a0f-a40f-1bde13bd4c22)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![WhatsApp Image 2025-10-19 at 06 37 52_77597857](https://github.com/user-attachments/assets/3f14e159-e9df-42d9-be34-c8ea7c6b2621)


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
![WhatsApp Image 2025-10-19 at 06 38 40_bc99b3b2](https://github.com/user-attachments/assets/dcf71c28-01c4-43e1-a979-ac80fc657866)

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
![WhatsApp Image 2025-10-19 at 06 38 06_8f8c2da3](https://github.com/user-attachments/assets/1d5c4cc7-c6ec-473e-8011-98a7653030b7)



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
![WhatsApp Image 2025-10-19 at 06 37 53_4a783fc3](https://github.com/user-attachments/assets/8963954d-3771-41c2-bff8-b371128e7e43)

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
![WhatsApp Image 2025-10-19 at 06 39 05_ce10e065](https://github.com/user-attachments/assets/9f743bad-fa61-4638-85c9-95bda0c1673b)


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
 ![WhatsApp Image 2025-10-19 at 06 38 55_a0b90266](https://github.com/user-attachments/assets/94c3a6aa-44a5-4ae0-844f-6e528be6bf04)

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
 ![WhatsApp Image 2025-10-19 at 06 39 06_b83de1ce](https://github.com/user-attachments/assets/b929a139-2b86-41b6-9775-3941b388d1dd)

 
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
 
 ![WhatsApp Image 2025-10-19 at 06 39 08_a0f19b7b](https://github.com/user-attachments/assets/c6fe7fa4-ef31-4a2c-b6a9-cce3fa8f5b9a)

 
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
 
 ![WhatsApp Image 2025-10-19 at 06 40 28_7cad6bdd](https://github.com/user-attachments/assets/a545c590-95b2-402b-a34f-731bc1faf400)

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
 ![WhatsApp Image 2025-10-19 at 06 40 29_f2557656](https://github.com/user-attachments/assets/cc7c224d-2988-4453-ad46-c4126aaaf144)

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
![WhatsApp Image 2025-10-19 at 06 40 29_6e6e6d9c](https://github.com/user-attachments/assets/0ee93838-ba57-4f42-9d3d-9163c02780b9)

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
<img width="697" height="233" alt="image" src="https://github.com/user-attachments/assets/3ab40f48-b075-4b54-abe1-4b92e46bdc5d" />


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
![WhatsApp Image 2025-10-19 at 06 40 17_dad35214](https://github.com/user-attachments/assets/ae762d48-da10-4037-8387-8ed108d37e5e)

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
![WhatsApp Image 2025-10-19 at 06 40 18_445fc830](https://github.com/user-attachments/assets/ef453e34-7286-4113-bbf2-5bed87ed132f)

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

 ![WhatsApp Image 2025-10-19 at 06 40 22_be6f139c](https://github.com/user-attachments/assets/fafa980c-0606-418b-b75e-01b0732d1e1e)

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
 ![WhatsApp Image 2025-10-19 at 06 40 23_24698b25](https://github.com/user-attachments/assets/82519b71-84a3-47c3-acb9-08791b659a3c)

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
 ![WhatsApp Image 2025-10-19 at 06 40 26_85dca63a](https://github.com/user-attachments/assets/22bab4c0-e5f8-4a85-8116-f9ec3dc560f8)

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
![WhatsApp Image 2025-10-19 at 06 40 25_ddac34ab](https://github.com/user-attachments/assets/36645d09-3114-4431-ae06-49c84cf88248)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![WhatsApp Image 2025-10-19 at 06 40 25_d77e624e](https://github.com/user-attachments/assets/2f5e3bec-5603-436d-822e-0490ab19740f)



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

 ![WhatsApp Image 2025-10-19 at 06 40 24_0e9716c0](https://github.com/user-attachments/assets/14c1dbf8-ae44-49a8-a6a9-b0a1ece71c65)

 ./funcex.sh 1 2

 <img width="775" height="38" alt="image" src="https://github.com/user-attachments/assets/cefde3b1-2d77-407c-9bb1-0c6c1a5aa2cc" />

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
![WhatsApp Image 2025-10-19 at 06 40 15_d26661e8](https://github.com/user-attachments/assets/93091437-039c-40c6-bcf5-b2eefd08d1ec)

 
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
![WhatsApp Image 2025-10-19 at 06 40 15_d57cb498](https://github.com/user-attachments/assets/d64d8e0a-934f-478b-94b4-8c8aafd0d89f)

 
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
 ![WhatsApp Image 2025-10-19 at 06 40 14_59a49e38](https://github.com/user-attachments/assets/22f57e0a-6bdb-4d38-a7be-b8f327fbb4ae)

 
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
 ![WhatsApp Image 2025-10-19 at 06 40 13_7393b75a](https://github.com/user-attachments/assets/77a3b0eb-5883-4c90-a088-de33379a00bb)

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

![WhatsApp Image 2025-10-19 at 06 40 12_70dc04eb](https://github.com/user-attachments/assets/87bf4bd3-b48d-4630-accb-7f9325b2448c)

# RESULT:
The Commands are executed successfully.

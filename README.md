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

<img width="456" height="243" alt="Screenshot from 2025-09-24 20-43-31" src="https://github.com/user-attachments/assets/560a7aed-179a-4eb2-92ad-1a4205c68d8c" />


cat < file2
## OUTPUT

<img width="475" height="296" alt="Screenshot from 2025-09-24 20-45-11" src="https://github.com/user-attachments/assets/d0b65bd2-3387-41ed-b7f0-86ba49ed3cca" />


# Comparing Files
cmp file1 file2
## OUTPUT

<img width="637" height="105" alt="Screenshot from 2025-09-24 20-46-17" src="https://github.com/user-attachments/assets/cbce947c-30c7-44ae-8f0f-9ada8e7f955d" />

 
comm file1 file2
 ## OUTPUT

<img width="617" height="190" alt="Screenshot from 2025-09-24 20-47-20" src="https://github.com/user-attachments/assets/2ccd66f3-cf18-45a9-9df6-4e9919b0d17a" />

 
diff file1 file2
## OUTPUT

<img width="616" height="216" alt="Screenshot from 2025-09-24 20-47-59" src="https://github.com/user-attachments/assets/c4adefab-ef1e-49a6-88fa-230322970241" />



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

<img width="644" height="100" alt="Screenshot from 2025-09-24 20-53-17" src="https://github.com/user-attachments/assets/3c41c727-ad1e-4266-922a-5debb09db60b" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="640" height="123" alt="Screenshot from 2025-09-24 20-54-32" src="https://github.com/user-attachments/assets/b1389f41-a439-4a26-94cf-94fd541e2da4" />


cut -d "|" -f 2 file22
## OUTPUT

<img width="640" height="123" alt="Screenshot from 2025-09-24 20-55-10" src="https://github.com/user-attachments/assets/5e093ed6-fe19-426a-b4ce-6032abbeaf63" />


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

<img width="638" height="139" alt="Screenshot from 2025-09-24 20-56-34" src="https://github.com/user-attachments/assets/955a70c1-7a0f-4e78-8bf8-1a12d9c05069" />


grep hello newfile 
## OUTPUT


<img width="654" height="64" alt="Screenshot from 2025-09-24 20-57-29" src="https://github.com/user-attachments/assets/650bef4d-9b34-414d-a87d-ef595de457f2" />


grep -v hello newfile 
## OUTPUT

<img width="648" height="87" alt="Screenshot from 2025-09-24 20-58-12" src="https://github.com/user-attachments/assets/0f9d895d-237e-4ad5-ad85-ed63cc6c1238" />


cat newfile | grep -i "hello"
## OUTPUT


<img width="648" height="87" alt="Screenshot from 2025-09-24 20-59-07" src="https://github.com/user-attachments/assets/5d8f0213-8b81-46d8-b99a-a7dcdd3be5bf" />


cat newfile | grep -i -c "hello"
## OUTPUT

<img width="658" height="71" alt="Screenshot from 2025-09-24 20-59-50" src="https://github.com/user-attachments/assets/4bf4d6d8-674e-4afc-ace3-60dc2e4ace43" />



grep -R ubuntu /etc
## OUTPUT

<img width="1295" height="990" alt="Screenshot from 2025-09-24 21-01-33" src="https://github.com/user-attachments/assets/b0732dfc-61f8-4a94-87ef-25da285df793" />


grep -w -n world newfile   
## OUTPUT

<img width="999" height="81" alt="Screenshot from 2025-09-24 21-02-58" src="https://github.com/user-attachments/assets/baa6b781-65df-49c9-9b8e-199201f2ad08" />


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

<img width="999" height="81" alt="Screenshot from 2025-09-24 21-06-07" src="https://github.com/user-attachments/assets/f92bb100-a534-493e-b200-668f25af4711" />


egrep -w '(H|h)ello' newfile 
## OUTPUT

<img width="999" height="81" alt="Screenshot from 2025-09-24 21-07-11" src="https://github.com/user-attachments/assets/f958f249-8f2b-41d8-bc8a-809fbd392ca0" />


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

<img width="999" height="81" alt="Screenshot from 2025-09-24 21-08-24" src="https://github.com/user-attachments/assets/169e988b-f861-4e55-a40a-da5c8f34c86f" />



egrep '(^hello)' newfile 
## OUTPUT

<img width="1001" height="67" alt="Screenshot from 2025-09-24 21-09-28" src="https://github.com/user-attachments/assets/22cc534e-c1ad-4ed6-9c6e-c8f2c80cc91d" />


egrep '(world$)' newfile 
## OUTPUT

<img width="1002" height="103" alt="Screenshot from 2025-09-24 23-23-08" src="https://github.com/user-attachments/assets/b89740bb-d1aa-4125-be22-757c30fd54c3" />


egrep '(World$)' newfile 
## OUTPUT

<img width="1002" height="48" alt="Screenshot from 2025-09-24 23-25-54" src="https://github.com/user-attachments/assets/00b8a50f-a051-4f8d-a763-31d3862c4d61" />


egrep '((W|w)orld$)' newfile 
## OUTPUT

<img width="1002" height="105" alt="Screenshot from 2025-09-24 23-27-07" src="https://github.com/user-attachments/assets/39f5768a-186c-4c7a-82eb-c18487c001e2" />


egrep '[1-9]' newfile 
## OUTPUT

<img width="1002" height="66" alt="Screenshot from 2025-09-24 23-27-56" src="https://github.com/user-attachments/assets/fbe138c2-35a0-4062-b8f6-6f63b1959ddd" />


egrep 'Linux.*world' newfile 
## OUTPUT

<img width="1002" height="84" alt="Screenshot from 2025-09-24 23-28-51" src="https://github.com/user-attachments/assets/e01aacac-39d2-4655-806d-72ecf3311ee5" />


egrep 'Linux.*World' newfile 
## OUTPUT

<img width="1002" height="50" alt="Screenshot from 2025-09-24 23-29-49" src="https://github.com/user-attachments/assets/1525250c-6425-4eae-aeac-c5ea10726a9c" />


egrep l{2} newfile
## OUTPUT

<img width="1002" height="85" alt="Screenshot from 2025-09-24 23-30-27" src="https://github.com/user-attachments/assets/145e5310-4bd1-4799-ac50-d71f6cba0be0" />


egrep 's{1,2}' newfile
## OUTPUT 

<img width="1002" height="104" alt="Screenshot from 2025-09-24 23-31-14" src="https://github.com/user-attachments/assets/adb5dc49-2903-467e-904d-462b79402c7c" />


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

<img width="1002" height="67" alt="Screenshot from 2025-09-25 08-04-40" src="https://github.com/user-attachments/assets/21cc64df-105b-4d75-8b9f-25c6fc7df29f" />


sed -n -e '$p' file23
## OUTPUT

<img width="1002" height="67" alt="Screenshot from 2025-09-25 08-06-20" src="https://github.com/user-attachments/assets/9b5e7fb0-cadf-4acf-a0a1-d6f9417e8c4b" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT

<img width="1002" height="214" alt="Screenshot from 2025-09-25 08-07-21" src="https://github.com/user-attachments/assets/2f4b21d8-cfac-4b3c-8f59-c073932a7f9f" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1002" height="214" alt="Screenshot from 2025-09-25 08-08-10" src="https://github.com/user-attachments/assets/fa9cc5b5-c74c-4205-a294-f16feb0e16da" />


sed  '/tom/s/5000/6000/' file23
## OUTPUT

<img width="1002" height="214" alt="Screenshot from 2025-09-25 08-09-09" src="https://github.com/user-attachments/assets/e69f0b3a-41d1-472a-afd5-10143bc2b42e" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="1002" height="143" alt="Screenshot from 2025-09-25 08-09-50" src="https://github.com/user-attachments/assets/c7fe23d8-6bf3-45a7-97a3-ea06b5bd3adf" />


sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="1002" height="104" alt="Screenshot from 2025-09-25 08-10-41" src="https://github.com/user-attachments/assets/7605ac28-2544-43da-9518-a1ae74d6d852" />



sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="1002" height="85" alt="Screenshot from 2025-09-25 08-12-07" src="https://github.com/user-attachments/assets/2c53d141-e7e2-4d16-8010-6c3ccaed6467" />


seq 10 
## OUTPUT

<img width="1002" height="223" alt="Screenshot from 2025-09-25 08-12-39" src="https://github.com/user-attachments/assets/df069252-7bbf-49f5-86b8-ce02dacbc7e7" />


seq 10 | sed -n '4,6p'
## OUTPUT

<img width="1001" height="108" alt="Screenshot from 2025-09-25 08-13-23" src="https://github.com/user-attachments/assets/500b58c6-5617-4872-8433-51c42a0b5651" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="1001" height="108" alt="Screenshot from 2025-09-25 08-14-06" src="https://github.com/user-attachments/assets/998cdc9c-7a3e-48b1-b912-610040c058a4" />


seq 3 | sed '2a hello'
## OUTPUT
<img width="1002" height="116" alt="Screenshot from 2025-09-25 08-15-11" src="https://github.com/user-attachments/assets/6ab41150-4733-4c4b-9fda-30f95ec06754" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="1002" height="116" alt="Screenshot from 2025-09-25 08-19-56" src="https://github.com/user-attachments/assets/ba66b7f1-d10a-48bc-aaf8-92d5acf44154" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="1002" height="103" alt="Screenshot from 2025-09-25 08-21-00" src="https://github.com/user-attachments/assets/6342e395-b55d-4cee-9972-eb43a7d2ecbb" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="1002" height="103" alt="Screenshot from 2025-09-25 08-23-26" src="https://github.com/user-attachments/assets/31e9200e-53ab-4380-8a77-818e66a9462c" />


sed -n '2,4{s/$/*/;p}' file23
##OUTPUT

<img width="1002" height="103" alt="Screenshot from 2025-09-25 08-24-33" src="https://github.com/user-attachments/assets/d0955cba-c954-4b9f-b2e3-d9e5d91ab061" />


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

<img width="1002" height="157" alt="Screenshot from 2025-09-25 08-27-08" src="https://github.com/user-attachments/assets/8512c61a-0aab-4949-9437-6cf7ed0ad9fc" />


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

<img width="1002" height="157" alt="Screenshot from 2025-09-25 08-30-38" src="https://github.com/user-attachments/assets/10342121-1fce-4624-ae33-bbfbbd820b17" />


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

<img width="1002" height="212" alt="Screenshot from 2025-09-25 08-31-32" src="https://github.com/user-attachments/assets/4906f828-10d6-44e3-8053-9f0eaf22fa61" />


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

<img width="1002" height="105" alt="Screenshot from 2025-09-25 08-34-12" src="https://github.com/user-attachments/assets/ea0e866f-f83a-430b-8399-31ae2167aabc" />

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

<img width="1002" height="105" alt="Screenshot from 2025-09-25 08-35-04" src="https://github.com/user-attachments/assets/b03da236-6b37-4c71-a932-89d83c798645" />


#Backup commands
tar -cvf backup.tar *
## OUTPUT



mkdir backupdir

<img width="1002" height="51" alt="Screenshot from 2025-09-25 08-37-05" src="https://github.com/user-attachments/assets/cf88585f-afe8-4c74-a460-48762d482c48" />

 
mv backup.tar backupdir

cd backupdir

<img width="1002" height="51" alt="Screenshot from 2025-09-25 08-39-01" src="https://github.com/user-attachments/assets/89218567-4aae-4fe4-9642-faa8ff34c156" />

 
tar -tvf backup.tar
## OUTPUT


tar -xvf backup.tar
## OUTPUT

gzip backup.tar

ls .gz
## OUTPUT
 
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

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT


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

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
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

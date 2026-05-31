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
<img width="2169" height="678" alt="1" src="https://github.com/user-attachments/assets/703242bf-ae90-4de9-bedb-0d86eb6bf7d3" />



cat < file2
## OUTPUT
<img width="1691" height="930" alt="2" src="https://github.com/user-attachments/assets/8934ab3a-59f2-4085-8a60-6655effbc58f" />


# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="2166" height="726" alt="3" src="https://github.com/user-attachments/assets/fa88d22b-0a5c-404c-9119-21f16272e937" />

comm file1 file2
 ## OUTPUT
<img width="1851" height="850" alt="4" src="https://github.com/user-attachments/assets/093f8660-0a58-46d2-b5b9-47af15c2303c" />

 
diff file1 file2
## OUTPUT
<img width="1540" height="1021" alt="5" src="https://github.com/user-attachments/assets/a34d40fa-24d3-469e-890e-fb0e322cef2e" />


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
<img width="1868" height="842" alt="6" src="https://github.com/user-attachments/assets/4ccd44c4-2c88-4f06-82a3-34a358476afd" />



cut -d "|" -f 1 file22
## OUTPUT

<img width="1884" height="835" alt="7" src="https://github.com/user-attachments/assets/2ea0bc8a-c0ba-4300-9740-4c6fe452a798" />


cut -d "|" -f 2 file22
## OUTPUT
<img width="1024" height="1536" alt="8" src="https://github.com/user-attachments/assets/8c804877-75a1-462c-b0a6-c53b093b7d58" />


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
<img width="2171" height="407" alt="9" src="https://github.com/user-attachments/assets/ff47d402-3547-40af-b7bc-003e2ddf83fb" />



grep hello newfile 
## OUTPUT
<img width="2007" height="511" alt="10" src="https://github.com/user-attachments/assets/f6083577-973b-40e0-89e2-60649ffd2433" />




grep -v hello newfile 
## OUTPUT
<img width="2007" height="511" alt="10" src="https://github.com/user-attachments/assets/e61e4a33-a454-4d3c-ad78-8a693fbf156e" />



cat newfile | grep -i "hello"
## OUTPUT
<img width="2171" height="352" alt="11" src="https://github.com/user-attachments/assets/17e7b6e3-22b5-4a3f-8eab-614129927b6b" />




cat newfile | grep -i -c "hello"
## OUTPUT
<img width="802" height="533" alt="image" src="https://github.com/user-attachments/assets/b8024c0c-3753-463e-972c-9ba8028077f2" />

grep -R ubuntu /etc
## OUTPUT
<img width="1394" height="410" alt="12" src="https://github.com/user-attachments/assets/c0a7431e-88c7-4319-be30-5732fd847c64" />


grep -w -n world newfile   
## OUTPUT
<img width="1792" height="488" alt="13" src="https://github.com/user-attachments/assets/ee6eff0c-44dc-4c29-be90-f4628e7b250d" />


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
<img width="1886" height="480" alt="14" src="https://github.com/user-attachments/assets/773b13de-cbef-4494-baad-98e58a42aa39" />

egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="2149" height="558" alt="15" src="https://github.com/user-attachments/assets/047989f2-db5a-4753-a41c-08bf5349d472" />

egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="2173" height="420" alt="16" src="https://github.com/user-attachments/assets/225851a8-085c-4242-bc3f-a06aff1a89c4" />


egrep '(^hello)' newfile 
## OUTPUT
<img width="2143" height="298" alt="19" src="https://github.com/user-attachments/assets/6798ee7d-7317-4055-8a19-c828fafed428" />



egrep '[1-9]' newfile 
## OUTPUT
<img width="2167" height="449" alt="20" src="https://github.com/user-attachments/assets/43373f93-c75d-4f76-a43b-aa26c4ec0dcb" />



egrep 'Linux.*world' newfile 
## OUTPUT
<img width="2167" height="449" alt="20" src="https://github.com/user-attachments/assets/6cb774b7-168e-442d-aac5-82a33bd32728" />


egrep 'Linux.*World' newfile 

<img width="1774" height="491" alt="22" src="https://github.com/user-attachments/assets/8afe517a-9339-45e1-8900-08a751995654" />
## OUTPUT

egrep l{2} newfile
## OUTPUT
<img width="1774" height="491" alt="22" src="https://github.com/user-attachments/assets/1328d2ba-b563-4aa1-9533-c4da31509815" />

egrep 's{1,2}' newfile
## OUTPUT 


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


<img width="302" height="47" alt="24" src="https://github.com/user-attachments/assets/a85b6a13-ee09-43f4-8413-c3b74cf7b729" />


sed -n -e '$p' file23
## OUTPUT


<img width="527" height="283" alt="25,26" src="https://github.com/user-attachments/assets/146ef50f-8a4d-4cd5-bf0f-04d8cf261571" />


sed  -e 's/Ram/Sita/' file23
## OUTPUT


<img width="527" height="283" alt="25,26" src="https://github.com/user-attachments/assets/a3930e0a-5710-4095-a75f-03aed7314714" />


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

<img width="1601" height="982" alt="27" src="https://github.com/user-attachments/assets/ff405bbc-b2e1-4dad-9a07-62537ad9d4e5" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT


<img width="1601" height="982" alt="27" src="https://github.com/user-attachments/assets/e09f3744-52d5-4b4f-b48d-da40004b7357" />


sed -n -e '1,5p' file23
## OUTPUT

<img width="1601" height="982" alt="27" src="https://github.com/user-attachments/assets/dc75172a-af54-4757-ae4e-a35be9a15ead" />



sed -n -e '2,/Joe/p' file23
## OUTPUT

<img width="1601" height="982" alt="27" src="https://github.com/user-attachments/assets/e8c1bac1-d25e-41ec-bea5-5104efe08fa1" />




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

<img width="313" height="339" alt="28" src="https://github.com/user-attachments/assets/36b3fba3-b3a6-47fd-80fc-28c5bdf55dcb" />



seq 10 
## OUTPUT

<img width="397" height="118" alt="29" src="https://github.com/user-attachments/assets/003c3dd1-7a35-4859-971e-c1000188935e" />

seq 10 | sed -n '4,6p'
## OUTPUT
<img width="396" height="84" alt="30" src="https://github.com/user-attachments/assets/ba5c85b1-a26e-47ba-9e2c-363374685748" />


seq 10 | sed -n '2,~4p'
## OUTPUT

<img width="2115" height="744" alt="31" src="https://github.com/user-attachments/assets/543c7cf7-8d0a-44e3-93b2-d71b96707e94" />



seq 3 | sed '2a hello'
## OUTPUT

<img width="2115" height="744" alt="31" src="https://github.com/user-attachments/assets/821c6976-38c2-4460-aa55-70d3bc94742f" />



seq 2 | sed '2i hello'
## OUTPUT

<img width="2112" height="744" alt="32" src="https://github.com/user-attachments/assets/76d913be-a004-4dba-8515-88722a8b3ae5" />


seq 10 | sed '2,9c hello'
## OUTPUT

<img width="491" height="131" alt="33" src="https://github.com/user-attachments/assets/fffd01d4-aff6-4092-b477-f82fc65168f4" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

<img width="491" height="131" alt="33" src="https://github.com/user-attachments/assets/d8590147-af5b-45da-8bd4-65924af8f75f" />



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



#Using tr command

cat file23 | tr [:lower:] [:upper:]
## OUTPUT
<img width="462" height="209" alt="35" src="https://github.com/user-attachments/assets/8677a363-d873-492e-ab37-cd066872ca62" />

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
<img width="419" height="247" alt="34" src="https://github.com/user-attachments/assets/cb9e8484-cdf5-4228-97b9-664b9055292a" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="419" height="247" alt="34" src="https://github.com/user-attachments/assets/81d49210-c563-4a18-b68d-a2ce9ad2547c" />



#Backup commands
tar -cvf backup.tar *
## OUTPUT
<img width="439" height="264" alt="36" src="https://github.com/user-attachments/assets/a6d66f6b-58f4-4c53-b29b-e4e8c2e7ee33" />


mkdir backupdir
 
mv backup.tar backupdir

cd backupdir
 
tar -tvf backup.tar
## OUTPUT
<img width="1457" height="1080" alt="37" src="https://github.com/user-attachments/assets/3df68c72-c29d-4abe-bf7e-62949cb4f68e" />


tar -xvf backup.tar
## OUTPUT
<img width="526" height="244" alt="Screenshot 2026-05-31 133703" src="https://github.com/user-attachments/assets/0d876558-eda0-4b62-a783-a17c5c058086" />


gzip backup.tar

ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
<img width="286" height="19" alt="image" src="https://github.com/user-attachments/assets/64198d31-3b87-4845-8433-b0a84d74a1ec" />

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="662" height="147" alt="image" src="https://github.com/user-attachments/assets/58b1b409-3f97-41ac-9584-1a942c82d8fd" />

 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="2115" height="744" alt="31" src="https://github.com/user-attachments/assets/ab93f90d-89de-4811-890e-7eaaef548b63" />


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
<img width="405" height="42" alt="Screenshot 2026-05-31 134741" src="https://github.com/user-attachments/assets/a0838d8c-387b-4f48-99da-0f2a0dd4b631" />

 
ls file1
## OUTPUT
<img width="329" height="66" alt="Screenshot 2026-05-31 134815" src="https://github.com/user-attachments/assets/76e73bd4-7c3e-42fc-860c-65b30af78fec" />

echo $?
## OUTPUT 
<img width="415" height="64" alt="image" src="https://github.com/user-attachments/assets/56b53470-132d-484c-b063-1e1e6695df84" />


./onebash: ./one: Permission denied
 
echo $?

 
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
<img width="1531" height="1027" alt="45" src="https://github.com/user-attachments/assets/5d5c090b-505e-487c-8876-1a96b415c1b5" />

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="1531" height="1027" alt="45" src="https://github.com/user-attachments/assets/8ef8608c-fc2e-49e2-b839-6e1a1b902c46" />


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
**<img width="772" height="493" alt="Screenshot 2026-05-31 135150" src="https://github.com/user-attachments/assets/f4895401-93c9-470f-8039-3acfec7daeed" />
**
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
<img width="1784" height="882" alt="46" src="https://github.com/user-attachments/assets/e361c83a-8991-4b3a-8888-460a234675aa" />



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
<img width="672" height="119" alt="image" src="https://github.com/user-attachments/assets/4b198b08-56f3-4ec7-81ab-212a315c77de" />

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
<img width="750" height="180" alt="Screenshot 2026-05-31 140946" src="https://github.com/user-attachments/assets/2c11c9f3-94b9-434e-bbbb-516837c53139" />

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
<img width="1531" height="1027" alt="45" src="https://github.com/user-attachments/assets/5e97f2a9-24be-407b-ad9f-9867527659ec" />

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
<img width="742" height="310" alt="Screenshot 2026-05-31 141107" src="https://github.com/user-attachments/assets/bab78489-dfa1-44be-a8be-032cffe4b8cc" />

 
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
<img width="1413" height="1113" alt="47" src="https://github.com/user-attachments/assets/0831a9e2-e9c7-4d75-9be8-8da7056c764e" />

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
<img width="746" height="333" alt="Screenshot 2026-05-31 141338" src="https://github.com/user-attachments/assets/e192bb28-0de6-4170-b33f-f36f2453d99f" />


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
<img width="1427" height="1102" alt="48" src="https://github.com/user-attachments/assets/5437f66c-866a-41d6-a87f-eb73ef021fab" />

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
<img width="1404" height="1120" alt="49" src="https://github.com/user-attachments/assets/6b3987d5-a879-49e0-82f5-963146e2a0df" />

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
<img width="1439" height="1093" alt="50" src="https://github.com/user-attachments/assets/c22eb700-94ef-41ab-883f-579decbb3907" />

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
<img width="837" height="1069" alt="51" src="https://github.com/user-attachments/assets/317ce0b5-81f8-4635-a1ce-12ed8b45297c" />

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
<img width="1354" height="1162" alt="53" src="https://github.com/user-attachments/assets/2c9769d3-0ca9-4db7-ac16-8b764072ec37" />


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
<img width="1354" height="1162" alt="53" src="https://github.com/user-attachments/assets/0a459fc0-353f-4a82-ba5a-4f3d9c16e72e" />



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
 <img width="435" height="409" alt="image" src="https://github.com/user-attachments/assets/d802309e-48ec-456a-9d28-70a8a217c39b" />

 
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
<img width="454" height="465" alt="Screenshot 2026-05-31 143154" src="https://github.com/user-attachments/assets/6cb1161f-76b0-487b-985e-ccecc51b15f5" />

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
<img width="1934" height="712" alt="last" src="https://github.com/user-attachments/assets/3bad3f54-7385-430f-9d84-d74be02e245c" />


# RESULT:
The Commands are executed successfully.

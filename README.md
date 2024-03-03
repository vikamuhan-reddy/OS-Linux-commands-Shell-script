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
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/720e1a2b-797d-4bae-af91-712e50df9fbe)



cat < file2
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/f70f4f43-0a94-4099-a0f2-a539ce786226)



# Comparing Files
cmp file1 file2
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/fd27fdb2-7f09-44ed-a1b8-0244b94d462b)


comm file1 file2
 ## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/107ba8ae-2f99-4ce0-a214-a38f3c260a07)


 
diff file1 file2
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/014a56a3-63c8-458b-ad9f-26760cc41a78)



#Filters

### Create the following files file11, file22 as follows:

cut -c1-3 file11
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/dc2a628f-8419-4ca4-bd1a-c2b462344b70)


cut -d "|" -f 1 file22
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/d6597249-7cc7-435f-a03a-e31d7429ed74)


cut -d "|" -f 2 file22
## OUTPUT
cat < newfile 
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/23f368b5-bcd7-483f-8e84-71d23ddda220)


## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/d7e1d9e0-c452-47dc-b6b0-e1aee18cf859)


 
grep hello newfile 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/c0e9a132-d5ad-4922-8940-d1b3789028c9)


grep -v hello newfile 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/d3a91490-980c-4c75-a412-5a9e624f96ce)


cat newfile | grep -i "hello"
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/b1e5ac79-8a2c-476b-8f92-4ef1bfc75c25)


cat newfile | grep -i -c "hello"
## OUTPUT

grep -R ubuntu /etc
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/d3aa8240-41aa-420d-a767-8222d3c03b7d)


grep -w -n world newfile   
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/364ba43e-90d8-472f-aa4a-ac654fce4d2e)

egrep -w 'Hello|hello' newfile 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/35aa515c-d8b3-4a7a-a34b-2e06658d23b5)


egrep -w '(H|h)ello' newfile 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/56d16534-a54e-402f-a04d-07c037f551c2)


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/f5959fda-c216-4520-ad30-24825d3b5fa6)


egrep '(^hello)' newfile 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/71e535cc-e903-4327-9eba-a088c585f4ae)

egrep '(world$)' newfile 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/ab80cc75-ce12-4f14-ab5a-71dc1c57def2)

egrep '(World$)' newfile 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/016f0da3-dcfd-414e-85c9-782dea8acf33)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/dfb50868-035e-4fac-9389-429b575b7666)

egrep '[1-9]' newfile 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/fc640ad6-d608-475c-bfc8-bb19c1b343d0)

egrep 'Linux.*world' newfile 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/7864f31c-51ec-4ca9-9291-bfe746724352)


egrep 'Linux.*World' newfile 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/e2427372-9a2e-4a24-afa8-c25d392e5e09)


egrep l{2} newfile
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/0b5319ec-44ed-46f7-b7e8-1616984cdda7)


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
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/5d0ccaff-6cb8-43d3-9f7f-dcc66f1bb9ba)

sed -n -e '3p' file23
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/e09c6d00-9388-4c15-80c6-5f40d3dadc1a)


sed -n -e '$p' file23
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/7f9fdd90-190b-4b63-a147-5cb847b474e3)


sed  -e 's/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/3597c1a7-ec30-4060-a1dd-13c10dfa29cc)

sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/021ea5fe-6baf-4c40-b437-df4c5f13a351)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/86adcd08-0f63-44d6-8a83-e4c4db8c8ae4)


sed -n -e '1,5p' file23
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/a6ce9508-28e4-41c6-9779-e40d9f312b4c)

sed -n -e '2,/Joe/p' file23
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/859dc27c-8d21-44fa-a9bb-e5b8a6540d46)


sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/ec83359f-718f-4774-9250-10eb19bd71a5)

seq 10 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/73bd2873-a256-4653-9d7c-5441ac2146c1)


seq 10 | sed -n '4,6p'
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/4a647d26-156e-4866-9b1b-cd95337d7354)

seq 10 | sed -n '2,~4p'
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/a58fa556-064b-45a0-91ce-bbba0cf6dbbb)


seq 3 | sed '2a hello'
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/20eb62c0-1f82-4dbe-9c2d-b3b269b8bed7)


seq 2 | sed '2i hello'
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/a265b47d-542f-47cf-997f-bfb71e9a8d09)


seq 10 | sed '2,9c hello'
## OUTPUT

![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/2125d902-15e6-429e-a963-c79c22dbabd0)


## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/03e4a1b4-bf08-4bbb-95bd-cdd21ef60b80)


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
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/00bc255f-e34e-4e26-ba5a-8e0189872c3a)


## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/df1087fd-5f13-4767-ad0a-4809cf51887a)


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
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/5aba0e3a-d0e6-4840-9498-7b3d552ffb4c)


#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/880c9e64-0d2c-47cc-8752-999be6c7b86d)

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```

```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '
 ## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/2ca38b49-1174-402a-b5f0-6d48263aae88)

cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/b5e8e483-1f99-49a6-97cb-4c02a4c2bcad)


#Backup commands
tar -cvf backup.tar *
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/404f4c90-f568-4d05-9eb6-40daedceb376)

mkdir backupdir
mv backup.tar backupdir 
tar -tvf backup.tar
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/a0f4dc30-d268-4d7d-892a-a867b18ccbf1)

tar -xvf backup.tar

## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/701739e9-1989-4ab9-a616-b7d517a7f7aa)

# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/7bf1616d-81f2-4c49-9466-8947b6860292)


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
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/291be63f-ae11-411f-83ca-4c444eb223fa)


echo $?
## OUTPUT 
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/779a0af7-6ac2-4f7c-98f0-6c0cb9547e95)


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/30c73c76-32f6-4400-b0d0-a05ea2fcb117)

abcd
 
echo $?

 
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
vi 
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/6cf96add-19fe-4b63-903d-d828070eb89f)

chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/4634d9c8-408c-479e-beb0-65c6c3392025)

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
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/45bf2780-4319-4d37-8890-4ad3a6877394)


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
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/16d8875a-367a-4332-b730-cd7186bd6a20)


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
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/816b6994-1394-4fb2-9567-cdf58370687a)

vi

$ chmod 755 iftest.sh
 
$ ./iftest.sh 
## OUTPUT
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/832f62d4-35f7-48f2-bfbd-f89eadd3b1e1)


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
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/5416b4cd-61aa-4e53-a4b1-b66cdd0f3b6e)


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
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/69a899b2-4bdf-435a-9a62-8516b202d2e5)


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
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/6557f265-e9a5-4841-bd5f-dd2a0c8543ec)


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
 ## Output
 
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
 
  ## Output

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
 
 
 ## Output
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/25558638-0812-4ed3-bc9c-68f5c250bad2)


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
 
 ## Output
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/c65ff61b-1cb9-451a-bb14-ae7e7b3e3869)


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
## Output
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/93354d3a-e0f3-475d-b9f9-ad61e96db8cd)

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
  ## Output
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/c00b8627-e17f-4cbe-a39d-1a361d63d2e7)


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
  ## Output
![image](https://github.com/vikamuhan-reddy/OS-Linux-commands-Shell-script/assets/144928933/9955dc46-7665-4f1b-8da7-6c81ce94a3a7)


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
file ="cities"
for state in 'cat $file'
do
echo "Visit beautiful $file"
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

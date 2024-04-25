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
![Screenshot from 2024-02-26 21-09-51](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/1eb494cb-a303-471b-8b4e-b240cdfe1b59)



cat < file2
## OUTPUT
![Screenshot from 2024-02-26 21-15-04](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/d4afcda6-2094-447a-837c-476edd8fdf8e)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![Screenshot from 2024-02-26 21-16-03](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/88d6122b-f66b-4214-b605-bdb5d23e4c74)

comm file1 file2
 ## OUTPUT
![Screenshot from 2024-02-26 23-01-34](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/46ef3dcf-ab6d-4dc2-9450-dc6746252652)

 
diff file1 file2
## OUTPUT
![Screenshot from 2024-02-26 21-16-24](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/ce13bab7-dbb6-42bd-b57b-d15b3e72c30d)


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
![Screenshot from 2024-02-26 21-18-03](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/801a19d1-de7a-4ecf-bf44-7e04254cce6a)




cut -d "|" -f 1 file22
## OUTPUT
![Screenshot from 2024-02-26 21-18-39](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/139364e0-52c8-4b35-a7dd-3802e479fd4c)



cut -d "|" -f 2 file22
## OUTPUT
![Screenshot from 2024-02-26 21-27-20](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/91ab0909-2e42-43fb-b26c-34832466879c)


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
![Screenshot from 2024-02-26 21-28-07](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/2a08e925-e654-4c71-bae8-91b99f494ffb)



grep hello newfile 
## OUTPUT
![Screenshot from 2024-02-26 21-27-20](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/c932a4cf-c9cf-426e-8fd1-c1b50863b355)






grep -v hello newfile 
## OUTPUT
![Screenshot from 2024-02-26 21-28-07](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/3d73053c-bf51-46d1-b0e5-6598a6691fec)



cat newfile | grep -i "hello"
## OUTPUT
![Screenshot from 2024-02-26 21-28-47](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/ac8f20db-f5f9-4938-a8ef-8ec7ce612a87)




cat newfile | grep -i -c "hello"
## OUTPUT
![Screenshot from 2024-02-26 21-29-07](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/1d69452a-1895-4045-ab3c-69ecd16efd54)




grep -R ubuntu /etc
## OUTPUT
![Screenshot from 2024-02-26 21-30-22](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/786e7ffa-08c2-4754-94d2-396f9b4f3ed9)
![Screenshot from 2024-02-26 21-31-09](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/28ec43fa-f83f-4caa-a559-a6273e71fc10)



grep -w -n world newfile   
## OUTPUT
![Screenshot from 2024-02-26 21-32-19](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/48b81761-ff36-4a9f-b586-015fb40cadb7)


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
![Screenshot from 2024-02-26 21-33-37](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/3889ef89-2f89-4ba8-88bb-9e9c039d0c60)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![Screenshot from 2024-02-26 21-33-52](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/e35cba1f-5441-4131-897c-c0a0c406b324)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
![Screenshot from 2024-02-26 21-34-11](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/8feb7c43-ac16-41be-88f6-5be360182c0c)




egrep '(^hello)' newfile 
## OUTPUT
![Screenshot from 2024-02-26 21-34-24](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/4ae7369c-1ad2-4386-8078-b98d4f0e8cd0)



egrep '(world$)' newfile 
## OUTPUT
![Screenshot from 2024-02-26 21-34-41](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/aaabcace-7824-4c92-b92b-27d17a2341d0)



egrep '(World$)' newfile 
## OUTPUT
![Screenshot from 2024-02-26 21-35-13](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/1064141e-9d50-4cdd-b8b7-b09ac9e57286)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![Screenshot from 2024-02-26 21-35-25](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/6ce2b12a-419f-41df-9075-4cb73b824916)



egrep '[1-9]' newfile 
## OUTPUT
![Screenshot from 2024-02-26 21-35-43](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/f817e573-f6d8-4323-a0b6-4f6bd28fbc01)



egrep 'Linux.*world' newfile 
## OUTPUT
![Screenshot from 2024-02-26 21-36-12](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/88d69a14-dfdf-4518-ab65-aa1e2ff9890c)


egrep 'Linux.*World' newfile 
## OUTPUT
![Screenshot from 2024-02-26 21-36-29](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/eb4ce590-14df-4bd2-a91f-99e7773d1851)


egrep l{2} newfile
## OUTPUT
![Screenshot from 2024-02-26 21-36-43](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/0985f138-f300-4039-ada9-d1900145a82a)



egrep 's{1,2}' newfile
## OUTPUT 
![Screenshot from 2024-02-26 21-36-59](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/73eee3d2-9501-49f9-97a8-146f9579a99e)


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
![Screenshot from 2024-02-26 21-37-28](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/21c9ab5c-2a8f-4f6f-a68f-d597fb9f2dbd)



sed -n -e '$p' file23
## OUTPUT
![Screenshot from 2024-02-26 21-38-23](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/9d1fd4af-0f0d-4938-8d94-478127cf84a7)



sed  -e 's/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-02-26 21-45-21](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/27291c74-f61c-404e-9b01-b0360d133d66)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![Screenshot from 2024-02-26 21-45-38](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/c75474bb-28c8-413e-ad77-ee4cf8ec99f8)



sed  '/tom/s/5000/6000/' file23
## OUTPUT
![Screenshot from 2024-02-26 21-45-56](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/62fd9cba-ce28-47e5-b600-dc87ebc08b0e)



sed -n -e '1,5p' file23
## OUTPUT
![Screenshot from 2024-02-26 21-46-12](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/ed725b0d-a3b0-4ef9-8cd5-696f5b05420a)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![Screenshot from 2024-02-26 21-46-22](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/76039472-7270-4bfd-a7ea-bde08b438061)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![Screenshot from 2024-02-26 21-46-38](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/69622f4d-6303-422b-a673-7fa6c3cfb673)



seq 10 
## OUTPUT
![Screenshot from 2024-02-26 21-46-55](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/0fccf460-3ecc-499f-934f-ea8a1ac063e0)



seq 10 | sed -n '4,6p'
## OUTPUT
![Screenshot from 2024-02-26 21-47-09](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/b8f81ec3-cb99-468f-810b-3719565af3ca)



seq 10 | sed -n '2,~4p'
## OUTPUT
![Screenshot from 2024-02-26 21-47-31](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/4e2ec16e-28a5-4e8c-a13a-7f464fafa680)



seq 3 | sed '2a hello'
## OUTPUT
![Screenshot from 2024-02-26 21-47-42](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/48c104ce-e317-4971-b7e6-04f419c27e7f)



seq 2 | sed '2i hello'
## OUTPUT
![Screenshot from 2024-02-26 21-47-51](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/e1f3bc3e-9788-48d2-a86e-1fccdc24c65e)


seq 10 | sed '2,9c hello'
## OUTPUT
![Screenshot from 2024-02-26 21-48-05](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/f42bac5e-c851-482e-b4f3-8691f0c56f23)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![Screenshot from 2024-02-26 21-48-19](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/7994545e-a3b1-43d7-8605-398c2a74c52f)



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
![Screenshot from 2024-02-26 21-49-56](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/3755d1ca-017a-4336-bb09-34814fc3c6d3)


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
![Screenshot from 2024-02-26 21-50-34](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/4247c664-de69-401b-ab8e-2b45c7202716)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![Screenshot from 2024-02-26 21-50-54](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/9c0cd74b-1c49-4187-82e1-06188b3a5098)


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
![Screenshot from 2024-02-26 21-53-49](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/d43caf08-1cc2-47f0-ad81-257ce45a2c16)


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![Screenshot from 2024-02-26 21-54-10](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/dff63826-397c-4f34-b67b-875c69fb681f)




 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
![Screenshot from 2024-02-26 22-01-30](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/8e188215-257f-4339-9157-56db574026d4)

 


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
![Screenshot from 2024-02-26 22-03-12](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/9ad031b1-7004-487a-b244-196ddc8d7d1d)

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![Screenshot from 2024-02-26 22-03-33](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/f1de4b8a-86d1-4e34-a00f-fd938b7174ee)

abcd
 
echo $?
 ## OUTPUT
![Screenshot from 2024-02-26 22-03-48](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/77869837-f002-4579-8777-f5021188160a)


 
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
![Screenshot from 2024-02-26 22-04-25](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/0b38d72b-20f9-4e29-9a0c-737c9f8d27a5)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
![Screenshot from 2024-02-26 22-06-27](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/9203a2c0-2bc8-4567-8cbe-561aa7e9b2b4)


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
![Screenshot from 2024-02-26 22-12-57](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/a7a0c791-2834-409c-b0f4-ef7fb0c84063)

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
![Screenshot from 2024-02-26 22-14-00](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/d968134e-a3e9-4a27-921d-d8d22a05b3e6)



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
![Screenshot from 2024-02-26 22-15-34](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/4f8d729d-463a-495a-9aac-a78b38d74787)

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
![Screenshot from 2024-02-26 22-15-34](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/9ea854c4-0880-468d-839e-a22a6943fe10)

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
![Screenshot from 2024-02-26 22-17-14](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/e40eb29a-c2f3-45ff-890e-f17ec9112a17)


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
![Screenshot from 2024-02-26 22-18-38](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/7a4957fa-8fd4-4adc-8c1b-9db42d369e6e)

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
![Screenshot from 2024-02-26 22-19-19](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/a0317446-0fb0-4a16-adec-cf1a531aa87a)

![Screenshot from 2024-02-26 22-22-23](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/dbdf71e3-e393-4c27-9b15-5debf1ec6a5b)

![Screenshot from 2024-02-26 22-24-37](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/cca1900d-116c-4917-874a-3857fbdad35e)

![Screenshot from 2024-02-26 22-25-14](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/18dc49e8-fbdd-4be2-bae9-83ff906bbde9)

![Screenshot from 2024-02-26 22-26-02](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/f6550540-0bea-4d20-9a63-f7817021d316)





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
![Screenshot from 2024-02-26 22-22-23](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/9f1271a3-aaab-4725-86c3-0dc34f9e97a3)


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
![Screenshot from 2024-02-26 22-32-34](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/0ac1519d-e571-4a1f-8199-38fb1c3220a5)

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
![Screenshot from 2024-02-26 22-32-34](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/eef485e0-95f3-4236-9543-6a0dc5c6bb5f)

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
![Screenshot from 2024-02-26 22-33-21](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/985170da-0c41-4a8f-9b53-6419e1832ea9)

 
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
![Screenshot from 2024-02-26 22-34-06](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/85aeb2e0-90ef-498d-9c65-3c5741f124ae)

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
 ![Screenshot from 2024-02-26 22-35-43](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/2ec173ed-865f-446a-bd72-0425619110cf)

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
![Screenshot from 2024-02-26 22-36-50](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/9a8e3128-2263-4261-ab88-d9100dd259eb)


 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT
![Screenshot from 2024-02-26 22-38-01](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/90913e7f-43ba-4445-9f2f-7e2bfe2d5a2d)



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
![Screenshot from 2024-02-26 22-39-50](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/5ec344cb-f85b-416b-ab34-3d9d2446392f)

 
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
 ![Screenshot from 2024-02-26 22-40-35](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/8040ae16-1b37-460a-aa35-452a98858aac)

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
 ![Screenshot from 2024-02-26 22-40-35](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/7fb1ba9a-75c8-4e61-b365-5d5c2628cc9c)

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
 ![Screenshot from 2024-02-26 22-43-44](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/1b469634-e547-48b4-b7ee-0c2367283663)

 
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
 ![Screenshot from 2024-02-26 22-45-05](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/3723f85b-b9f8-42da-b83a-0152e2dbc08c)

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
![Screenshot from 2024-02-26 22-46-57](https://github.com/Kishorerz/OS-Linux-commands-Shell-script/assets/144451216/bedba6be-d944-4258-889e-aca0f83cf763)


# RESULT:
The Commands are executed successfully.

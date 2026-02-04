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
~~~
S.Vishvabala
SP.Swaminathan
S.Jayalakshmi
```
cat > file2
```
rithesh
bala
vishva
naresh
arasu
^d
```
### Display the content of the files
cat < file1
## OUTPUT
~~~
S.Vishvabala
SP.Swaminathan
S.Jayalakshmi
~~~

cat < file2
## OUTPUT
~~~
rithesh
bala
vishva
naresh
arasu
~~~
# Comparing Files
cmp file1 file2
## OUTPUT
~~~
 file1 file2 differ: byte 2, line 1
 ~~~
comm file1 file2
 ## OUTPUT
~~~
	ant
apple
banana
	bear
carrot
	cat
 ~~~
diff file1 file2
## OUTPUT
~~~
1,3c1,3
< apple
< banana
< carrot
---
> ant
> bear
> cat
~~~
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
~~~
Hel
Thi
~~~
cut -d "|" -f 1 file22
## OUTPUT
~~~
1001 
1002 
1003 
~~~
cut -d "|" -f 2 file22
## OUTPUT
~~~
Ram 
 tom 
 Joe
~~~
cat > newfile 
```
Hello world
hello world
^d
````
cat < newfile 
Hello world
hello world
 
grep Hello newfile 
## OUTPUT
~~~
<img width="348" height="51" alt="image" src="https://github.com/user-attachments/assets/3a4a5406-f880-4ad3-9b38-c32045c2aded" />

~~~
grep hello newfile 
## OUTPUT
~~~
<img width="348" height="51" alt="image" src="https://github.com/user-attachments/assets/f892ebef-0c5d-489b-8097-82469536cd84" />

~~~
grep -v hello newfile 
## OUTPUT
~~~
Hello world
~~~
cat newfile | grep -i "hello"
## OUTPUT
~~~
<img width="452" height="73" alt="image" src="https://github.com/user-attachments/assets/61528813-769f-440d-8ff2-47489f7a78b8" />

~~~
cat newfile | grep -i -c "hello"
## OUTPUT
~~~
2
~~~
grep -R ubuntu /etc
## OUTPUT
~~~
<img width="1843" height="930" alt="image" src="https://github.com/user-attachments/assets/ec4411c4-0592-47dc-a5b7-79b258adf4ed" />

~~~
grep -w -n world newfile   
## OUTPUT
~~~
<img width="389" height="80" alt="image" src="https://github.com/user-attachments/assets/9833447d-17cb-4e51-89d9-3046853d5b9c" />
~~~

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
~~~
<img width="451" height="72" alt="image" src="https://github.com/user-attachments/assets/94b5c50a-3eca-403c-aba6-334905aa0075" />

~~~
egrep -w '(H|h)ello' newfile 
## OUTPUT
~~~
<img width="451" height="72" alt="image" src="https://github.com/user-attachments/assets/1979e7b5-92cd-48c4-ba71-f36eab934383" />
~~~


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
~~~
<img width="467" height="75" alt="image" src="https://github.com/user-attachments/assets/2a8335f5-9dad-44bd-bc47-bce72141127e" />
~~~



egrep '(^hello)' newfile 
## OUTPUT
~~~
<img width="466" height="52" alt="image" src="https://github.com/user-attachments/assets/e9b28206-ad20-4597-96ee-09c6cf7d1248" />
~~~
egrep '(world$)' newfile 
## OUTPUT
![image-18](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/7facd439-94d3-4e5e-adb2-853ad1bd6bc7)



egrep '(World$)' newfile 
## OUTPUT

![image-19](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/40aa135b-3fa1-46aa-8253-6a703f7b48d5)


egrep '((W|w)orld$)' newfile 
## OUTPUT

![image-20](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/62209b33-310f-4386-aea3-d142a5c0810c)


egrep '[1-9]' newfile 
## OUTPUT

![image-21](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/0152c2fe-457b-4690-849a-f57756272f93)


egrep 'Linux.*world' newfile 
## OUTPUT

![image-22](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/60e8c4d1-ad89-41c6-bc59-29a898615219)


egrep 'Linux.*World' newfile 
## OUTPUT

![image-23](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/fcf5b29f-3e8e-486f-8c97-cbc0e84d45d8)


egrep l{2} newfile
## OUTPUT

![image-24](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/57fd296b-8124-46f5-809f-d604bf3f32a5)


egrep 's{1,2}' newfile
## OUTPUT 

![image-25](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/fd083fc1-9048-4442-9046-7b53de83095c)


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

![image-26](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/d9bd46cd-fdb6-4c13-844b-0a4ffedf951e)


sed -n -e '$p' file23
## OUTPUT

![image-27](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/f60eb1ea-a356-4a14-af2c-69503d475b02)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![image-28](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/3cce3526-d915-4693-a14a-80f4a88aabfc)



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
![image-29](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/29de2ae9-3534-41c6-b584-4fd63ea15230)



sed  '/tom/s/5000/6000/' file23
## OUTPUT

![image-30](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/27ff55dd-f7a8-4934-9234-af87f38063e4)


sed -n -e '1,5p' file23
## OUTPUT

![image-31](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/b72812ad-2031-4998-834f-d1aa4e7d6570)


sed -n -e '2,/Joe/p' file23
## OUTPUT
![image-32](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/481af551-915d-4ee4-affb-2528903d3535)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
![image-33](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/c4ce50db-b01c-48f0-b022-b0fdc8c46639)

seq 10 
## OUTPUT
![image-34](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/2e43f350-47fe-4f4f-b559-a5145bac13c6)


seq 10 | sed -n '4,6p'
## OUTPUT
![image-35](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/334cef52-f8dd-40f8-b811-edac5bfae54f)


seq 10 | sed -n '2,~4p'
## OUTPUT

![image-36](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/470d9aef-0a7d-4c6b-b67e-9442df4ad226)


seq 3 | sed '2a hello'
## OUTPUT

![image-37](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/beeb13d9-d0c1-4784-a4f5-5fe355900534)



seq 2 | sed '2i hello'
## OUTPUT

![image-38](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/8ae6ab60-f3ff-4190-a885-c2c5921e998f)


seq 10 | sed '2,9c hello'
## OUTPUT

![image-39](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/2a305976-182e-4c36-b54a-914fec39158b)


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT

![image-40](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/6a5520ed-5568-4a42-9647-6277d1b393a6)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![image-41](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/03038fff-d49a-4d7c-b043-130d202e2c08)

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

![image-42](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/b5c9289b-32c1-48ae-a0bd-e0c8be1193a8)


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

![alt text](image-43.png)

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

![image-43](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/724ba449-4db6-4631-9339-80dec3f97217)


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

![image-44](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/6f2cfae7-a399-46ab-bef0-dbdb43a9827f)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT

![image-46](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/ceadf916-c72c-4bcc-874b-2dc7ca9cc011)


#Backup commands
tar -cvf backup.tar *
## OUTPUT

![image-47](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/ade6e389-88d9-4e18-a2b5-9cad8eeab035)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![image-48](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/5bb41cc5-eb5a-4406-868d-b04a5929d057)


tar -xvf backup.tar
## OUTPUT

![image-49](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/7f0eb601-551f-47f1-8e00-eec94af72a6a)


gzip backup.tar

ls .gz
## OUTPUT
![image-50](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/493fb6bd-f365-4e5b-9f33-3bb16e4fa822)

 
gunzip backup.tar.gz
## OUTPUT

![image-51](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/a4c005dd-16b7-405e-a90d-f776c67834c0)

 
# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT

![image-52](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/54d1032c-fc93-4b9c-a049-81f72d2e7fd3)


 
cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT

![image-53](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/b0f6d3ac-1aab-401d-a68f-fac5190af59d)


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

![image-54](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/aa9e221b-1914-41c6-96a4-a3480fcc931c)

 
ls file1
## OUTPUT
![image-54](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/7aa3c8d8-08cf-4789-be3e-8eb056aec0c6)

echo $?
## OUTPUT 

![image-56](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/b392932f-12c9-47bf-9d86-fb44457adb34)


./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 
abcd
 
echo $?
 ## OUTPUT
![image-57](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/6cac1aec-beb9-4683-91ba-2a6e062a4fd3)


 
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

![image-58](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/f8e710dd-372f-4b4c-9db1-efd9aa88e581)


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![image-59](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/23f2ccf2-f9e4-4dff-98fc-0b3812c642a5)

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

![image-60](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/3a6c2ae0-7cf8-4ca0-8eb5-e174e8a1622e)


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
![image-61](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/7d9c90af-b7a3-4cf6-8965-40370727248e)



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
![image-62](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/f0646e68-4bbe-4c0e-bf34-7212526995d8)



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

![image-63](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/446feb99-72a9-496c-b9ac-42f9b0e0c6b6)


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

![image-64](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/a2ca4461-3b62-41b0-afa0-eb9523ebc501)


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

![image-65](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/8d68fc65-0b14-4777-af74-cefbc365c662)


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
 ## output

![image-66](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/bf4deead-473f-4b07-b440-bc1e6c3759dd)



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

![image-67](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/bacb7046-9079-489a-acff-43e650c8135d)

 
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


![image-68](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/34e7fcfa-aa6b-4a1b-a82c-a81ab7997f53)

 
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
 
 ## output:

![image-69](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/33272df2-f5b8-4bda-99f5-5a048690600c)

 
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
 
 ## output

![image-70](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/c51da2ea-8652-49c3-a893-f64acc51d52d)



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

##output

![image-71](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/ef2f1f17-feed-4357-a5a0-e63e33ea14be)




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

![image-72](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/3b304910-6ecf-4fa3-85ea-6dec124f087e)


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

![image-73](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/0a482550-5b9e-4ff8-9e33-54dc8ffa77a5)


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
![image-74](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/d60ca9a2-6750-4f0e-bd8a-bad4b996fbce)


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

![image-75](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/978f2ab3-ba04-442a-b668-62aa2450402e)


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

![image-76](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/cd016d47-b62c-4697-8211-2ccbb4e91301)

 
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
![image-77](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/25960989-f3d5-4a74-9eeb-ad4e77ea6755)


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

![image-78](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/33663a39-1b90-46dc-a249-29cce8e18d43)



 
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
![image-79](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/a353a7b2-7b6e-447f-99d8-eff19742bb64)



 
 ./funcex.sh 1 2
 ## output:
![image-80](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/c1b2d17b-036c-4d8b-b615-a4ae510d1db3)

 
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

![image-81](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/dc93f107-da58-4069-8676-fa8001a53772)

 
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

![image-82](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/e260570a-740d-40d6-b3d0-650cf1e0bfe6)

 
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
![image-85 (copy)](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/22c9f9e9-ae69-4152-9768-0122fe2f2a21)

 
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
 
![image-84](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/538413e2-0bfb-498f-bd90-181bb3e71a69)


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

![image-86](https://github.com/HIRU-VIRU/OS-Linux-commands-Shell-script/assets/145972122/736ba1b8-9102-4b04-bf53-666e03ad5961)

# RESULT:
The Commands are executed successfully.

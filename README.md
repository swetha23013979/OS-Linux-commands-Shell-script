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
![368667672-276a2699-7b6f-497d-a445-2c52e73ee176](https://github.com/user-attachments/assets/1de078b3-2ab0-4b83-b090-aca6a9215cf7)




cat < file2
## OUTPUT
![368667751-44e07fab-52e2-4865-86d2-8d8dc67e22d9](https://github.com/user-attachments/assets/228ec642-0835-4932-a3f7-4c20c90f3851)


# Comparing Files
cmp file1 file2
## OUTPUT
 ![368667854-3e9d92df-b80b-45cf-9f7a-c423d45a5dce](https://github.com/user-attachments/assets/23e66d39-a81e-469b-9a0d-13df54f7f972)

comm file1 file2
 ## OUTPUT

 ![368667943-d80adeab-e5bd-45d7-ba1a-88b4b3f070d6](https://github.com/user-attachments/assets/ab871b34-8107-4f4b-a29c-e0c116d8d940)

diff file1 file2
## OUTPUT
![368668031-897b57a3-5157-4b2d-b96b-598b85dbac8a](https://github.com/user-attachments/assets/353ade6d-bbac-4e89-8797-a1c381b8fc2b)


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
![368668217-3e542a9f-a842-4d01-8ea9-8a5f4002b3a1](https://github.com/user-attachments/assets/9e113b2a-b259-45d6-b224-65543c342065)




cut -d "|" -f 1 file22
## OUTPUT
![368668281-f12cfb17-daac-4ae5-8ddd-74bf00707e91](https://github.com/user-attachments/assets/b899d630-028d-4c47-a713-d53899bd1429)



cut -d "|" -f 2 file22
## OUTPUT
![368668377-22f7cf20-3c0c-4417-909e-8bcdc78a97f6](https://github.com/user-attachments/assets/ca1dee6e-7d84-4bc3-8b94-59be8ed6f021)


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

![368668458-2da9217e-ed9b-4be0-a585-6bfe3abc6275](https://github.com/user-attachments/assets/c2d35a46-bcb1-4900-aa1c-04dd3488396f)


grep hello newfile 
## OUTPUT

![368668546-630bf0a8-5698-46cd-9f7b-6e999b070074](https://github.com/user-attachments/assets/83e6e200-af11-494c-9229-4f1a18d8d161)



grep -v hello newfile 
## OUTPUT

![368668603-b03ee433-be87-4d6b-868b-a17a71c454a0](https://github.com/user-attachments/assets/f16d8e8d-37cb-4505-bcb2-e0009b9f1f9d)


cat newfile | grep -i "hello"
## OUTPUT
![368668679-e1abe671-97e0-4aea-b377-ce928af61f94](https://github.com/user-attachments/assets/85c590ee-40b7-4949-9514-5ba90747d0eb)




cat newfile | grep -i -c "hello"
## OUTPUT

![368668767-9b394c28-c744-4418-ab1a-2faeba22d92c](https://github.com/user-attachments/assets/a7ca785b-d2f7-489b-a3e2-5eb0f839598c)



grep -R ubuntu /etc
## OUTPUT

![368668830-6a561fd5-4a83-443c-89e2-afd8e4a9b188](https://github.com/user-attachments/assets/e6d850ac-681a-41fc-b1b3-98a0e064dc4f)


grep -w -n world newfile   
## OUTPUT

![368669114-2d3fed5a-c605-4a05-ad4e-aa18ec9a454f](https://github.com/user-attachments/assets/cbc56105-e927-436d-a488-a5b8a7010e42)

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
![368670030-d04b5d16-d946-446b-aaf1-3fdd4866418f](https://github.com/user-attachments/assets/4f7b2e37-b895-40db-91e3-ccbc58ee7435)



egrep -w '(H|h)ello' newfile 
## OUTPUT
![368670105-39f700c2-813d-4a34-9a4f-142d0d31dbea](https://github.com/user-attachments/assets/856820e7-d4e7-4542-9d12-77adbdc8bc2d)



egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT

![368670196-880e575e-d9f6-4763-93aa-47d0274dd357](https://github.com/user-attachments/assets/7106ca31-031d-45a0-883a-d188b1ab8b96)



egrep '(^hello)' newfile 
## OUTPUT

![368670276-e9f259af-5b88-4d89-bf95-fb3819dab4b1](https://github.com/user-attachments/assets/e84a367d-e24e-4f81-9f72-2628a76e8fa8)


egrep '(world$)' newfile 
## OUTPUT

![368670333-c48fb805-45e6-47e5-870d-ce9275c752e1](https://github.com/user-attachments/assets/01a927a7-5e9d-47af-825d-96945257321e)


egrep '(World$)' newfile 
## OUTPUT
![368670409-192fbf08-d8cb-4611-93c9-06a41f189a80](https://github.com/user-attachments/assets/69b360bb-ba79-4ba8-a88e-5d3b1eedbe01)


egrep '((W|w)orld$)' newfile 
## OUTPUT
![368670482-0da302fb-1e5e-4b4a-8999-731e777e7491](https://github.com/user-attachments/assets/a17fce72-a642-4569-abb5-82cb85f8cc32)



egrep '[1-9]' newfile 
## OUTPUT
![368670535-ba4540b2-6d81-4a4d-b85e-da7bad8bbbad](https://github.com/user-attachments/assets/81536227-4ecf-46da-8b24-42c30a222b80)



egrep 'Linux.*world' newfile 
## OUTPUT
![368670576-8c97e00e-f190-421a-8d9d-e62d5ae1cb72](https://github.com/user-attachments/assets/745152a1-f4a6-444d-92d7-2c268e9ed983)


egrep 'Linux.*World' newfile 
## OUTPUT
![368670652-291543bb-5a2f-49c0-9f9e-13881ea7b8bb](https://github.com/user-attachments/assets/fa5f31f7-e3cd-418f-90de-128652c864fa)


egrep l{2} newfile
## OUTPUT

![368670793-1b2b3740-cc02-4f0b-9950-7b89cc8b7bb6](https://github.com/user-attachments/assets/9c77e4cb-9ff9-4920-8df3-f1be7ab7bafd)


egrep 's{1,2}' newfile
## OUTPUT 
![368670843-1a09d193-1d07-4b24-8203-83a2c4d23428](https://github.com/user-attachments/assets/ecd14aac-8aa3-44b1-8c2d-b7631df5f7b1)


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

![368670893-c1dfff90-8839-4230-a5c9-16accbcc7f1e](https://github.com/user-attachments/assets/db092570-89f8-403d-a451-8eecec6104dd)


sed -n -e '$p' file23
## OUTPUT

![368670952-f96716f6-2c92-4c49-8a55-c373979f13a6](https://github.com/user-attachments/assets/0c08293c-64e1-44d4-b575-29b223c2a6ca)


sed  -e 's/Ram/Sita/' file23
## OUTPUT

![368671008-789d3263-a3cc-436f-9c01-3a3a68afe438](https://github.com/user-attachments/assets/ef3ebd75-4cc1-4227-b6a6-417ddef93fdf)


sed  -e '2s/Ram/Sita/' file23
## OUTPUT

![368671250-39004b75-1648-45aa-bd62-3a63350bc426](https://github.com/user-attachments/assets/1cd3006f-4771-45c9-a3dd-cd84fa5578ac)


sed  '/tom/s/5000/6000/' file23
## OUTPUT
![368671280-8da512b6-1699-4b88-8239-6241c4eb7098](https://github.com/user-attachments/assets/3113dcf4-249e-4c37-8b45-8df6b27c7e1a)



sed -n -e '1,5p' file23
## OUTPUT
![368671352-d42b4b6b-caf5-4bc7-970a-1e11dfa31d17](https://github.com/user-attachments/assets/a8c4378f-4213-47b3-b673-640007fad273)



sed -n -e '2,/Joe/p' file23
## OUTPUT
![368671426-aa3e6d8b-84bc-4bff-98a2-40e04b18d37b](https://github.com/user-attachments/assets/a0ef58a2-b04b-4fd8-afc0-006df6b70aff)




sed -n -e '/tom/,/Joe/p' file23
## OUTPUT

![368671460-8655fa0f-9032-4e35-a50d-1e2a053a9dc4](https://github.com/user-attachments/assets/650e2f3f-b79a-4ca9-9320-dbf0e27328a2)


seq 10 
## OUTPUT

![368671504-b1867c75-d70a-4e76-8e5d-e8524f2eb6a2](https://github.com/user-attachments/assets/5661446e-d9f3-4704-8cf5-818f5c0cacd7)


seq 10 | sed -n '4,6p'
## OUTPUT

![368671535-6cf52a41-cbd4-4002-a863-46904dda0431](https://github.com/user-attachments/assets/55e591bb-0d78-49b6-a311-8ee0892751f5)


seq 10 | sed -n '2,~4p'
## OUTPUT

![368671590-ea20efb3-8863-4821-9adf-3b0f5be31ad2](https://github.com/user-attachments/assets/2e0f6985-2585-4975-9dfe-5a6050677af8)


seq 3 | sed '2a hello'
## OUTPUT

![368671618-76c609c6-d43a-4202-9789-9b7cfb6ed9dc](https://github.com/user-attachments/assets/cc3ea790-12cc-4573-92b9-313c7feed3a3)


seq 2 | sed '2i hello'
## OUTPUT
![368671683-35a2d1ad-52f2-4904-8952-48b17b38a988](https://github.com/user-attachments/assets/96d2eab9-7e05-4d7a-97bf-f714b95c8722)


seq 10 | sed '2,9c hello'
## OUTPUT

![368671725-9ebfa007-13fa-4cd6-ab77-57c8a4101f80](https://github.com/user-attachments/assets/c223946b-513e-454a-a687-474174c84fe8)

sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
![368671787-1decb7ba-62d9-4e13-8666-f213b0e74004](https://github.com/user-attachments/assets/67e7699f-3aa3-44fa-9690-4c54b7272b50)



sed -n '2,4{s/$/*/;p}' file23
## OUTPUT

![368671847-5932714c-f4ea-4985-a9f4-8f1309e8ad45](https://github.com/user-attachments/assets/866cc957-ffca-4405-b2c2-069b062c287a)


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

![368672071-1b9cd914-a522-4416-b1bc-53f16445ded7](https://github.com/user-attachments/assets/fd6601b3-ad74-4578-835a-5b15caeacacd)

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
![368672119-f8232178-e836-4b6c-91ee-ad71d7576d49](https://github.com/user-attachments/assets/61334059-7a03-4006-acff-479b4fae0a77)



#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT
![368672165-ada97cf2-b333-4361-b059-7b72a42934e6](https://github.com/user-attachments/assets/5f3b7c53-7be1-45c3-9042-4bd13b28091f)

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

![368672228-3efafe75-3107-4244-b1fc-b88a680ff68d](https://github.com/user-attachments/assets/97c32406-2ce4-4a00-9229-35d81c79cf32)

 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
![368672270-e7f1cfe3-a6e9-4a96-a7ea-b84c15bc70db](https://github.com/user-attachments/assets/27609367-0279-4982-83aa-aecbf9d38b9f)



#Backup commands
tar -cvf backup.tar *
## OUTPUT
![368672309-3128ac3e-29dd-4ffb-afe5-d702c8457a54](https://github.com/user-attachments/assets/5b75f414-36ab-48d1-9087-9cfd0e0e2903)


mkdir backupdir
 
mv backup.tar backupdir
 
tar -tvf backup.tar
## OUTPUT

![368672354-b7d10414-d99f-4d64-9544-fc044a9f6232](https://github.com/user-attachments/assets/c72d1ae4-1b21-4c61-b692-ed8c5057ec4f)

tar -xvf backup.tar
## OUTPUT
![368672412-19150a72-2ff0-42b6-9cf1-19ce0cee6ae8](https://github.com/user-attachments/assets/976e8da0-2fe2-44c0-883b-107c393a85c4)

gzip backup.tar

## OUTPUT
 ![368672475-4e60d86b-db41-41e4-a2bd-ffa7d8065574](https://github.com/user-attachments/assets/37542227-c0d4-4bd3-aca4-9676993c7346)

gunzip backup.tar.gz
## OUTPUT
![368672857-5d80a72b-bde8-41b1-8fc7-1bc0eef7528d](https://github.com/user-attachments/assets/0863735d-2051-4034-b9e6-17f8f73e4d22)

## OUTPUT
![368672721-39001746-a8ac-446b-9ef8-a6363af484b0](https://github.com/user-attachments/assets/61d45c33-3e0b-43b7-8e0c-86cf7abf1bb9)


# Shell Script
```
echo '#!/bin/sh' > my-script.sh
echo 'echo Hello World‘; exit 0 >> my-script.sh
```
chmod 755 my-script.sh./my-script.sh
## OUTPUT
 ![368672939-0322b809-aedc-434f-87ed-8a7e0038ca56](https://github.com/user-attachments/assets/7c8f069a-2422-4740-b7b6-711a0cf26f42)

![368672967-a55c0d2c-89ee-4a54-8018-d2f04422ff03](https://github.com/user-attachments/assets/400adb32-1e47-444a-a5ac-022a41acd191)


cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
![368673009-f9bb98a2-241e-4a6c-bbef-45af5bde6882](https://github.com/user-attachments/assets/b7a24886-a9b5-421d-8e77-4764fffbae1f)


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
![368673069-7b57a072-05df-4077-8545-d2d3ff6adb42](https://github.com/user-attachments/assets/57a33e89-caa1-4750-89a7-15a8efd3ae60)

 
ls file1
## OUTPUT
![368673110-c441de58-ca42-499d-82e9-28bec1fe82da](https://github.com/user-attachments/assets/56a90d6c-ec46-4257-8cd4-4f4200445939)

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 
echo $?
## OUTPUT 
 ![368673138-c3114c7e-af18-4ce0-8349-dab9a0fb5436](https://github.com/user-attachments/assets/7fd5e5d7-aad1-43fb-88c6-4a17f2720159)


 
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
![368673507-3469b2e8-3c68-402e-bb0e-dc1c5e467891](https://github.com/user-attachments/assets/42d5f53a-bdd5-4355-a873-31a4226ad2dd)



chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT

![368673582-ecd9e8a0-003b-49de-8e0b-21afc33722d4](https://github.com/user-attachments/assets/5ecfb574-02dc-4369-942c-e385e1654322)


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
![368673663-db6d9268-e10e-46fb-b24a-c57d5d03bbdd](https://github.com/user-attachments/assets/9a3d9761-5bfe-4741-aea7-c1c5de97e0ea)

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

![368673736-5aee7d6e-970c-4236-ba6b-180a717ff917](https://github.com/user-attachments/assets/2d8ccb35-8e35-48a2-85da-788b1b1d9f5f)


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
![368673926-0d0f4252-20b0-4254-9670-2132f4525ee0](https://github.com/user-attachments/assets/fb9d76d1-e6bf-447a-8338-6b5138d98084)

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
![368674019-fab0300b-2022-4ad0-a3bd-9b3ac9eeee2c](https://github.com/user-attachments/assets/b30e479b-9dc2-4265-8f40-5f17d38cb5fb)

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
![368674080-33d8ce98-fcea-421b-96ad-f7510a391eaa](https://github.com/user-attachments/assets/119fae90-62f4-46af-b77a-7a6552272d33)


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
![368681485-9449f425-72b7-4c9c-bf39-bb3b36ee4a6e](https://github.com/user-attachments/assets/ad69a5f9-d2a8-4244-ada8-64b9c8858cbf)

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
![368681718-c1696d99-ba95-4fbd-87d2-68caa6a9fe1f](https://github.com/user-attachments/assets/01d52314-55d3-4d83-84a3-f80f9f55daba)


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
![368681903-c2274e30-fd57-49f3-a66d-3854567d23c7](https://github.com/user-attachments/assets/e42dc6a9-b8c7-42a3-ad46-60dab4e11cd7)


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
![368681990-27312fa1-741f-4968-8443-80393b19f7d7](https://github.com/user-attachments/assets/511e75b5-86d5-40a7-91ac-9c6f174b8beb)

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
![368682046-a134c06d-bc2f-47d6-8079-55a8d1099bd0](https://github.com/user-attachments/assets/ece56a79-f662-4aaf-a035-28c7f5e2d492)

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
![368682091-d473c5f2-88f2-47ad-bf72-36db4122db46](https://github.com/user-attachments/assets/882b4878-090f-4811-9e72-5e2b8fbfcc7c)

 
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
![368682168-80125046-a293-4f6d-a045-41e24a09659b](https://github.com/user-attachments/assets/db7747f6-aaf3-4f19-a4cd-28f5d204a673)

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
 ![368682336-a71f37e6-a7b7-4936-b6ac-d4d1df7c52cd](https://github.com/user-attachments/assets/be818f5a-8e00-4834-8d9a-265c25962b0c)

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

![368682402-88f36639-b54b-4c80-8d6f-35126e84e673](https://github.com/user-attachments/assets/f73afb6c-9488-49f6-a476-d47c54880133)

 cat exread1.sh
```bash
#!/bin/bash
# testing the read command
read -p "Enter your name: " name
echo "Hello $name, welcome to my program. “
``` 
$ chmod 755 exread1.sh 

## OUTPUT

![368682485-ac5a4a45-d04b-4748-ab7f-c6b5e1d6d381](https://github.com/user-attachments/assets/8c191cc0-6337-43a5-9c31-c3cbc036135b)


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
![368682576-ad721d8a-b4ae-4eab-81fa-8cef958b6421](https://github.com/user-attachments/assets/d0e58655-c5d9-4570-ac44-3a55e61814fe)

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

![368682702-cdc9d420-ac46-4688-a926-b017c1eb8106](https://github.com/user-attachments/assets/149da583-de0d-497f-8be0-f080cf76e27e)

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
![368682791-24b06404-63f9-4358-8f23-ba80165d2f22](https://github.com/user-attachments/assets/48c55da9-4083-445a-9c07-59b23da64d5a)


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
![368682863-4d226e69-fd6b-4322-8e04-359eccb5b146](https://github.com/user-attachments/assets/0b333a67-cbce-4796-809a-97ceeec2c403)

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
 ![368682925-0913aaaf-815c-43e5-8a68-67d378785123](https://github.com/user-attachments/assets/6a345e6a-3730-42b3-9ef7-13e493c49e10)

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

![368682998-892623f1-936a-4c9a-8fb0-6bdfcf70f9ab](https://github.com/user-attachments/assets/d5b97f74-2e43-40d3-899c-50e0558475fe)

![368683019-1acacb37-ab32-4a18-85f8-90048c3b8bcd](https://github.com/user-attachments/assets/232c955b-d3e8-41cc-b577-37278c19bfa1)


# RESULT:
The Commands are executed successfully.

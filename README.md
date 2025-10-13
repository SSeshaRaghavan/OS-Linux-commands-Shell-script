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
<img width="175" height="122" alt="Screenshot 2025-10-07 133359" src="https://github.com/user-attachments/assets/0d3a412a-cce6-411f-8c03-2f0812e4c37e" />





cat < file2
## OUTPUT
<img width="179" height="140" alt="Screenshot 2025-10-07 133407" src="https://github.com/user-attachments/assets/a645961e-a862-4f70-9a3e-3ac06a4b3741" />

# Comparing Files
cmp file1 file2
## OUTPUT
 <img width="280" height="72" alt="Screenshot 2025-10-07 133416" src="https://github.com/user-attachments/assets/ad1787aa-aff7-42e0-bd91-3d9a2d362a60" />

comm file1 file2
 ## OUTPUT
<img width="291" height="201" alt="Screenshot 2025-10-07 133428" src="https://github.com/user-attachments/assets/3f3366bb-0cc9-4444-9964-228670befbcd" />

 
diff file1 file2
## OUTPUT
<img width="195" height="220" alt="Screenshot 2025-10-07 133436" src="https://github.com/user-attachments/assets/e91c0013-a797-4d6b-a4bc-8ba1aa8b017e" />


#Filters

### Create the following files file11, file22 as follows:

cat > file11
```
Hello world
This is my world
^d
```
<img width="176" height="85" alt="Screenshot 2025-10-07 134655" src="https://github.com/user-attachments/assets/a239f8ab-712b-434d-a2dc-3d1b068d1393" />

cat > file22
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
^d
```
<img width="255" height="93" alt="Screenshot 2025-10-07 134709" src="https://github.com/user-attachments/assets/f61f46eb-6e79-4745-89ed-54e9e1b28b2b" />



cut -c1-3 file11
## OUTPUT
<img width="179" height="72" alt="Screenshot 2025-10-07 134715" src="https://github.com/user-attachments/assets/6d21761a-fb6f-48d5-8209-4d8d9e7daae4" />




cut -d "|" -f 1 file22
## OUTPUT
<img width="218" height="90" alt="Screenshot 2025-10-07 134722" src="https://github.com/user-attachments/assets/33029520-8162-4799-8e30-b95fa7485ccf" />



cut -d "|" -f 2 file22
## OUTPUT
<img width="222" height="94" alt="Screenshot 2025-10-07 134731" src="https://github.com/user-attachments/assets/59891ac0-3b26-45a8-b88a-7f26ad2fc930" />


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
<img width="175" height="71" alt="Screenshot 2025-10-07 134800" src="https://github.com/user-attachments/assets/ca47ac10-54d4-497e-a28c-bc1201b009ff" />



grep hello newfile 
## OUTPUT




grep -v hello newfile 
## OUTPUT



cat newfile | grep -i "hello"
## OUTPUT




cat newfile | grep -i -c "hello"
## OUTPUT




grep -R ubuntu /etc
## OUTPUT



grep -w -n world newfile   
## OUTPUT


cat < newfile 
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```
<img width="239" height="119" alt="Screenshot 2025-10-07 152300" src="https://github.com/user-attachments/assets/b78d9991-7c78-4c5f-9d07-2fe71f4ac101" />

cat > newfile
```
Hello world
hello world
Linux is world number 1
Unix is predecessor
Linux is best in this World
^d
```
<img width="243" height="124" alt="Screenshot 2025-10-07 152306" src="https://github.com/user-attachments/assets/803e4b89-fea9-40f4-b32d-a93d4e3b602c" />

egrep -w 'Hello|hello' newfile 
## OUTPUT
<img width="280" height="68" alt="Screenshot 2025-10-07 152313" src="https://github.com/user-attachments/assets/37ec5711-1ac5-408c-b270-9cdba2e1ec75" />


egrep -w '(H|h)ello' newfile 
## OUTPUT
<img width="268" height="73" alt="Screenshot 2025-10-07 152323" src="https://github.com/user-attachments/assets/1a86b834-0e4b-4d37-8bf8-060f31df2d80" />				


egrep -w '(H|h)ell[a-z]' newfile 
## OUTPUT
<img width="295" height="67" alt="Screenshot 2025-10-07 152335" src="https://github.com/user-attachments/assets/9d4309e9-fd8a-40c6-830b-312c8f983fca" />


egrep '(^hello)' newfile 
## OUTPUT
<img width="254" height="55" alt="Screenshot 2025-10-07 152345" src="https://github.com/user-attachments/assets/be18ec07-e66f-419b-803c-2b08a519b3ab" />


egrep '(world$)' newfile 
## OUTPUT
<img width="254" height="69" alt="Screenshot 2025-10-07 152356" src="https://github.com/user-attachments/assets/51ef2362-d91e-4552-b425-6da18c899789" />


egrep '(World$)' newfile 
## OUTPUT
<img width="254" height="69" alt="Screenshot 2025-10-07 152356" src="https://github.com/user-attachments/assets/486eacc6-2820-4f58-9017-7e77cccca835" />

egrep '((W|w)orld$)' newfile 
## OUTPUT
<img width="288" height="89" alt="Screenshot 2025-10-07 152406" src="https://github.com/user-attachments/assets/45c479e1-3920-432f-9a37-67770b5aad62" />


egrep '[1-9]' newfile 
## OUTPUT
<img width="234" height="58" alt="Screenshot 2025-10-07 152412" src="https://github.com/user-attachments/assets/efb61647-b06b-406f-8dd0-47cf94249acf" />


egrep 'Linux.*world' newfile 
## OUTPUT
<img width="286" height="57" alt="Screenshot 2025-10-07 152420" src="https://github.com/user-attachments/assets/a89a6d10-9022-4311-a704-5f5ce4be918e" />

egrep 'Linux.*World' newfile 
## OUTPUT
<img width="289" height="53" alt="Screenshot 2025-10-07 152426" src="https://github.com/user-attachments/assets/bfaa0074-6ea8-46f7-96fa-274eb6dbf861" />


egrep l{2} newfile
## OUTPUT



egrep 's{1,2}' newfile
## OUTPUT 
<img width="231" height="101" alt="Screenshot 2025-10-07 152929" src="https://github.com/user-attachments/assets/a935a82c-f117-4da5-8629-07a9d41a9efc" />

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
<img width="267" height="173" alt="Screenshot 2025-10-07 152935" src="https://github.com/user-attachments/assets/07c142d7-ddc6-4c71-aac4-1ba627d01b71" />

sed -n -e '3p' file23
## OUTPUT
<img width="223" height="61" alt="Screenshot 2025-10-07 152940" src="https://github.com/user-attachments/assets/155d9126-653d-45e2-9af9-ef0343545f62" />



sed -n -e '$p' file23
## OUTPUT
<img width="208" height="62" alt="Screenshot 2025-10-07 152946" src="https://github.com/user-attachments/assets/524b682d-afff-44b9-be1e-b7f0cb2eb1f7" />



sed  -e 's/Ram/Sita/' file23
## OUTPUT
<img width="260" height="169" alt="Screenshot 2025-10-07 152955" src="https://github.com/user-attachments/assets/59044966-a271-4a10-bfb7-fb6304ec8721" />



sed  -e '2s/Ram/Sita/' file23
## OUTPUT
<img width="260" height="166" alt="Screenshot 2025-10-07 153030" src="https://github.com/user-attachments/assets/74a5557a-2b5e-47ef-9910-146ff81a0f74" />



sed  '/tom/s/5000/6000/' file23
## OUTPUT
<img width="320" height="179" alt="Screenshot 2025-10-07 153037" src="https://github.com/user-attachments/assets/733e2caf-e8e2-4cd9-a358-c4bbd8035458" />



sed -n -e '1,5p' file23
## OUTPUT
<img width="269" height="123" alt="Screenshot 2025-10-07 153043" src="https://github.com/user-attachments/assets/656980bb-7567-4dbe-948e-fcc2e2886177" />


sed -n -e '2,/Joe/p' file23
## OUTPUT
<img width="257" height="151" alt="Screenshot 2025-10-07 153320" src="https://github.com/user-attachments/assets/d4d080d3-278e-4d33-8832-c7ad475aa1a1" />

sed -n -e '/tom/,/Joe/p' file23
## OUTPUT
<img width="300" height="141" alt="Screenshot 2025-10-07 153329" src="https://github.com/user-attachments/assets/6e121952-339a-43d4-8b9f-e2fe103d8555" />


seq 10 
## OUTPUT
<img width="185" height="197" alt="Screenshot 2025-10-07 153336" src="https://github.com/user-attachments/assets/838f4583-ee44-4f15-88da-c5115eadbe24" />

seq 10 | sed -n '4,6p'
## OUTPUT
<img width="222" height="96" alt="Screenshot 2025-10-07 153342" src="https://github.com/user-attachments/assets/b7707b73-b0af-49a1-bc42-12b856890ea9" />


seq 10 | sed -n '2,~4p'
## OUTPUT
<img width="223" height="91" alt="Screenshot 2025-10-07 153348" src="https://github.com/user-attachments/assets/211995ea-f841-4306-9d7f-1b30949bd491" />

seq 3 | sed '2a hello'
## OUTPUT
<img width="234" height="222" alt="Screenshot 2025-10-07 153403" src="https://github.com/user-attachments/assets/873b0f91-a5bf-42b2-b56c-cbde6063ee0e" />

seq 2 | sed '2i hello'
## OUTPUT
<img width="236" height="213" alt="Screenshot 2025-10-07 153409" src="https://github.com/user-attachments/assets/5dfe28ad-b775-4ea8-8cf9-a3ab706f2faa" />

seq 10 | sed '2,9c hello'
## OUTPUT
<img width="235" height="88" alt="Screenshot 2025-10-07 153416" src="https://github.com/user-attachments/assets/5f4355a1-b5d9-483e-8832-c30a98ea8b7f" />


sed -n '2,4{s/^/$/;p}' file23
## OUTPUT
<img width="274" height="89" alt="Screenshot 2025-10-07 153715" src="https://github.com/user-attachments/assets/02763097-429c-459e-88ff-0564f4ffff5b" />

sed -n '2,4{s/$/*/;p}' file23

<img width="272" height="97" alt="Screenshot 2025-10-07 153721" src="https://github.com/user-attachments/assets/5e2080d6-dd32-49a2-9676-92da4241f70b" />


#Sorting File content
cat > file21
```
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
<img width="249" height="124" alt="Screenshot 2025-10-07 153729" src="https://github.com/user-attachments/assets/9e8e60cd-af16-4b78-afa3-056498fe0ae2" />

sort file21
## OUTPUT
<img width="257" height="124" alt="Screenshot 2025-10-07 153736" src="https://github.com/user-attachments/assets/349a657c-cf09-4374-a1fd-6a2afb7f8488" />

cat > file22
```
1001 | Ram | 10000 | HR
1001 | Ram | 10000 | HR
1002 | tom |  5000 | Admin
1003 | Joe |  7000 | Developer
1005 | Sam |  5000 | HR
1004 | Sit |  7000 | Dev
```
<img width="262" height="140" alt="Screenshot 2025-10-07 153743" src="https://github.com/user-attachments/assets/076bc87b-7dff-4273-b86a-9c392c01575b" />

uniq file22
## OUTPUT
<img width="247" height="137" alt="Screenshot 2025-10-07 154111" src="https://github.com/user-attachments/assets/a27afb2f-e53f-4323-9450-962f8bab2713" />

#Using tr command

cat file23 | tr [:lower:] [:upper:]
 ## OUTPUT

cat < urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
^d
 ```
<img width="181" height="87" alt="Screenshot 2025-10-07 154124" src="https://github.com/user-attachments/assets/a4eb595c-0b23-4879-b67b-4619aebee321" />

cat > urllist.txt
```
www. yahoo. com
www. google. com
www. mrcet.... com
 ```
cat urllist.txt | tr -d ' '

 ## OUTPUT
<img width="258" height="107" alt="Screenshot 2025-10-07 154134" src="https://github.com/user-attachments/assets/ebeaf8bd-4059-49e7-a092-0381ed9ab56d" />


 
cat urllist.txt | tr -d ' ' | tr -s '.'
## OUTPUT
<img width="360" height="82" alt="Screenshot 2025-10-07 154144" src="https://github.com/user-attachments/assets/8dd131c4-f9c2-4578-91aa-6413f32cda9b" />

#Backup commands
tar -cvf backup.tar *
## OUTPUT

<img width="398" height="333" alt="Screenshot 2025-10-07 160048" src="https://github.com/user-attachments/assets/62b95776-0308-4ced-8ce9-335bc0ecc86b" />

mkdir backupdir

mv backup.tar backupdir

<img width="255" height="94" alt="Screenshot 2025-10-07 160058" src="https://github.com/user-attachments/assets/58f42a5f-2e1c-48a3-99f2-c815511417c8" />

cd backupdir

<img width="226" height="48" alt="Screenshot 2025-10-07 160106" src="https://github.com/user-attachments/assets/99c11d3b-fae4-4276-973a-de5f1566a72b" />

tar -tvf backup.tar
## OUTPUT
<img width="456" height="95" alt="Screenshot 2025-10-07 160118" src="https://github.com/user-attachments/assets/6cf64a46-25eb-4884-a58f-0dd02364a85d" />

tar -xvf backup.tar
## OUTPUT

<img width="459" height="83" alt="Screenshot 2025-10-07 160126" src="https://github.com/user-attachments/assets/76db08b3-723e-4b31-aa9d-08413e58fd1b" />

gzip backup.tar

<img width="360" height="66" alt="Screenshot 2025-10-07 161208" src="https://github.com/user-attachments/assets/7f749c17-6759-4e33-9c90-88c1428ffbd8" />


ls .gz
## OUTPUT
 
gunzip backup.tar.gz
## OUTPUT
<img width="383" height="71" alt="Screenshot 2025-10-07 161215" src="https://github.com/user-attachments/assets/073e8281-0bb0-4db7-ad7f-903b0af13014" />

# Shell Script
```
echo #!/bin/sh > 
echo echo Hello World; exit 0 
```
chmod 755 my-script.sh
./my-script.sh
## OUTPUT
<img width="292" height="45" alt="Screenshot 2025-10-07 162050" src="https://github.com/user-attachments/assets/cb6ad78b-1501-4eda-bdf2-ca9ba25d6f13" />

 <img width="254" height="71" alt="Screenshot 2025-10-07 162059" src="https://github.com/user-attachments/assets/9603c131-029c-4729-be6f-a9289f9dd048" />

cat << stop > herecheck.txt
```
hello in this world
i cant stop
for this non stop movement
stop
```

cat herecheck.txt
## OUTPUT
<img width="263" height="119" alt="Screenshot 2025-10-07 162316" src="https://github.com/user-attachments/assets/0800fbce-f77e-4674-8326-4d68c71d5b48" />


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
<img width="311" height="245" alt="Screenshot 2025-10-07 162554" src="https://github.com/user-attachments/assets/f8fa19ef-74d7-4192-a278-42f9134fcf90" />
<img width="275" height="244" alt="Screenshot 2025-10-07 162601" src="https://github.com/user-attachments/assets/fdfc9c51-6492-4d2d-90e5-3fd06132fe22" />
,<img width="310" height="94" alt="Screenshot 2025-10-07 162611" src="https://github.com/user-attachments/assets/46682083-79de-40f8-94fe-c2ba59d98539" />

 
ls file1
## OUTPUT

echo $?
## OUTPUT 
./one
bash: ./one: Permission denied
 <img width="178" height="130" alt="Screenshot 2025-10-08 134337" src="https://github.com/user-attachments/assets/8595df18-1824-48b9-b8b7-d4096a0e0b4c" />

echo $?
## OUTPUT 
 <img width="166" height="60" alt="Screenshot 2025-10-08 134345" src="https://github.com/user-attachments/assets/452b6808-a1f9-47f7-9f9c-ac1687875ed3" />

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
<img width="283" height="183" alt="Screenshot 2025-10-08 134315" src="https://github.com/user-attachments/assets/85671503-a45b-49a2-9f96-b9de8bb386fe" />
<img width="288" height="186" alt="Screenshot 2025-10-08 134325" src="https://github.com/user-attachments/assets/6f775bd1-6ab3-4b85-b184-58b96ebca414" />


chmod 755 strcomp.sh
 
./strcomp.sh 
## OUTPUT
<img width="325" height="136" alt="Screenshot 2025-10-08 134438" src="https://github.com/user-attachments/assets/2f52a7f8-cab0-4c0a-a8a5-4c23f2ff6718" />


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
<img width="486" height="379" alt="Screenshot 2025-10-08 134606" src="https://github.com/user-attachments/assets/5bbe9eb9-3804-486f-9de9-a3a82d117b1e" />

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
<img width="433" height="845" alt="Screenshot 2025-10-08 134916" src="https://github.com/user-attachments/assets/60e26ec7-a703-4956-a2d8-8e5e9702d33d" />



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
<img width="371" height="657" alt="Screenshot 2025-10-08 135120" src="https://github.com/user-attachments/assets/40929668-8d17-45fe-a6d9-fc26542e505e" />

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
<img width="439" height="460" alt="Screenshot 2025-10-08 135550" src="https://github.com/user-attachments/assets/9998e2e4-c02a-4a2b-aaf9-d76e68aec91e" />


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
<img width="390" height="450" alt="Screenshot 2025-10-08 135610" src="https://github.com/user-attachments/assets/f7652190-fad8-46ee-a908-37460f80657d" />

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
<img width="469" height="555" alt="Screenshot 2025-10-08 135626" src="https://github.com/user-attachments/assets/0f36b90d-4c51-4f9b-b297-e21a1d1423c7" />
 
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
 <img width="235" height="610" alt="Screenshot 2025-10-08 140038" src="https://github.com/user-attachments/assets/2cbbc8e1-99fa-4f45-a904-d636f79604fc" />

 
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
<img width="295" height="694" alt="Screenshot 2025-10-08 140051" src="https://github.com/user-attachments/assets/d6fc5235-8f43-4083-a740-a7b84c845e31" />
 
 
 
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

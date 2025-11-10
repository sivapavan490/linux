1. commandname --help
    <command name><options><inputs>
2. Generating the public key and private key
```
ssh-keygeen -f <filename>
```
ex:- ssh-keygen -f siva

3. Login to the server using private key
```
ssh -i <privatekeyfilename>  username@publicip
```

ex:- ssh -i siva.pem ec2-user@184.72.71.255 

4.Download the file in linux using brlow 2 commands
```
wget <URL> -->  Downloads the file
curl <URL> --> Shows the content on the screen #it will not download the file it will just showa on the screen.
curl <URL> -o <file name> --> donwloads the file with name given
``` 

5. How to use cut and awk command.

```
https://raw.githubusercontent.com/DAWS-82S/notes/refs/heads/main/session-02.md

/ --> seperator/delimiter/fragments
Sivakumar Reddy M

piping

grep <word-to-search> <file>

| --> pipe

cat <file-name> | grep <word-to-search>

cut command:-
=============

```
cut -d "seperator or delimiter or fragment" fragment no
```

ex:- echo "https://raw.githubusercontent.com/DAWS-82S/notes/refs/heads/main/session-02.md" | cut -d "/" -f9
session-02.md

awk command
=============
echo "https://raw.githubusercontent.com/DAWS-82S/notes/refs/heads/main/session-02.md" | awk -F "/" '{print $NF}'

echo "https://raw.githubusercontent.com/DAWS-82S/notes/refs/heads/main/session-02.md" | awk -F "/" '{print $1F}'

How can I get all the users in Linux Servers

awk -F ":" '{print $1F}' passwd
```

6. USING FIND COMMAND  TO IDENTFY THE FILE OR FOLDER IN LINUX

```
find <which-location> -name "<file-name>"

find / -name "passwd"
```
7. command or : mode & insert mode commands
```
command mode
----------------
:q --> quit
:wq --> write and quit
:q! --> force quit without changes
:/<word-to-find> --> search the word from top to bottom
:?<word-to-find> --> search the word from bottom to top
:noh --> no highlight
:set nu --> set line numbers in the file
:set nonu --> dont set line numbers
:28 d --> deleted 28th line
:3s/word-to-find/word-to-replace --> replaces first occurenece in that line
:3s/word-to-find/word-to-replace/g --> replaces all occureneces in that line
:%s/word-to-find/word-to-replace/g --> replaces all occureneces in file
:%d --> delete entire content

ESC Mode
---------------
u --> undo
yy --> copy the line
p --> paste
10p --> paste the lines 10 times
dd --> cut the line
gg --> takes to top
shift+g --> takes to bottom
```

# user creation
```
useradd username
```
# password setting
```
passwd username
```
# To create new group
```
groupadd groupname
```
# Adding user to primary group
```
usermod -g groupname username
```

# Adding user to secondary group
```
usermod -aG groupname username
```

# Deleting the user
```
userdel username
```
# deleting $ creating the group
```
groupdel groupname
groupadd groupname
```

# for changing file permiisions
```
chmod ugo filename
```

# for changing owner permisions
```
chown user:group filename/foldername
```
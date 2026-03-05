<h1> Linux Users & Permissions </h1>

```console 
User Categories:
    -Superuser Account - unrestrcited permissions 
    -User Account - regular user in /home/tom
    -Service Account - relevant for Linux Server Distros 
        -each service gets its own user
        -mysql user start mysql application
```

<h3> How to manage Permissions </h3>

```console 
1. User Level: give permissions to directly 

2. Group Level: group users into Linux Groups 
```

<h3> Access Control Files </h3>

```console 
1. /etc/passwd: stores user account info
    -adduser/useradd tom 
    -userdel/deluser
    -passwd [user]: changes user password
    
 -usermod [OPTIONS] [username]: modifys a user account 
    -usermod -g devops tom: make devops the primary group of user tom

-usermod -G admin,system,etc [user]
    -usermod -G admin tom: adds user to secondary group

2. /etc/shadow: 

3. /etc/group
    -groupadd/addgroup [group_name]: create new group 
    -delgroup/groupdel [user]: removes user from a group
    -gpasswd -d [user] [group]: removes a user from a specified group
```

<h2> File Permissions & Ownership </h2>

<h3> Ownership </h3>

```console 
ls -l: prints files in a long listing format showing permissions 
ls -la: shows hidden files 

chown [username]:[groupname] [filename]: changes ownership 

chgrp [groupname] [filename]: changes just the group of the filename 
```

<h3> Ways to set permissions </h3>

```console 
drwx-rwxr-x
rwx: user
rwx: group
r-x: others

r: read
w: write
x: execute 

a dash instead of the letter means the permission is absent 

1. Symbolic Mode: use of +/-
chmod -x [filename/directory]- removes execute permission for everyone 
chmod g-w [filename/directory] - removes write permission for group 
chmod g+w [filename/directory] - add write permission for group

chmod g=rwx [filename]- add read,write,& execute for that specific file group
chmod o=r-- [filenamae] - gives read permision only to others

2. Numeric Mode
read: 4
write: 2
execute: 1

chmod 777 [filename]- gives read,write, and execute permissions 
```

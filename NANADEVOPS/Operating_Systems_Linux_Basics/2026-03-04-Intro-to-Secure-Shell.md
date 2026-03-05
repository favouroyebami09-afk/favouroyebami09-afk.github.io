<h1> Introduction to SSH </h1>

```console 
SSH - Secure Shell 
2 Ways to Authenticate:
a. username & password
b. SSH Key Pair 
    -client machine connecting to the remote creates an SSH Key pair
    -key pair are private + public 
    -private key = secret key. is stored securely on the client machine 
    -public key can be shared. it is shared with the remote server 

SSH can be used for services as well
    Services like Jenkins often need to connect to anothe server via SSH

Communication must be allowed via firewall and port 22 
SSH server runs on port 22 by default 

Demo Overview:
1. Create remote server on cloud platform
2. Generate SSH key pair on our laptop
3. Copy Bash Script file to the remote server 
```

<h3> DEMO of SSH </h3>

```console
1. Create the remote server on DigitalOcean
    -choose password authentication 

2. SSH into the remote server via a Linux CLI
    -ssh UserName@SSHserver
    -ssh root@<public-ip-address>
    -select default for every prompts 

3. Now generate a SSH key pair on the linux (client) terminal 
     -ssh-keygen -t [option]: option is the type of key pair being generated
     -ssh-keygen -t rsa: accepts all default configuration
     ~/.ssh is the default location for a ssh key pair 

4. Confirm the creation of the keys 
    -ls .ssh/
    -id_rsa = private key
    -id_rsa.pub = public key

5. Copy the public key from the client
    -cat .ssh/id_rsa.pub
    -copy this key

6. Add the public key to the remote server 
    -ls .ssh
    -vi .ssh/authorized_keys
    -paste the public key from client into .ssh/authorized_keys
    -save it 
    -exit from the remote server 

7. Verify by trying to SSH again after exiting 
    -ssh root@<pulic-ip-address>


Note on the SSH syntax
-ssh root@<public-ip-address> is the SAME AS
-ssh -i .ssh/id_rsa root@<pulic-ip-address>
    its using the DEFAULT private IP from the .ssh/id_rsa folder
```

<h3> Copy the Bash Script </h3>

```console
8. Create a bash script on the client 
    -vi test.sh
    [#!/bin/bash
    echo "I am executed on the remote server"]

9. Copy the bash script file from client to remote 
    -scp test.sh root@<public-ip-address>:/root OR
    -scp -i .ssh/id_rsa test.sh root@<public-ip-address>:/root

**scp (secure copy) = llows you to secure copy files and directories
**secure meaning files and password are encrypted

10. SSH into remote server and verify the bash script
     -ssh root@<public-ip-address>
     -ls -l 

11. Give it executable permission and execute
    -chmod u+x test.sh
    -./test.sh
```




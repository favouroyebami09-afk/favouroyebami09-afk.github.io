<h1> Environmental Variables </h1>

```console
Environment variables are available for the whole environment 
By convention, names are defined in UPPER CASE
SHELL=/bin/bash
HOME=/home/nana
USER=nana

User can change these environment variable values
```

<h3> List all Env. Variables </h3>

```console
printenv: displays all the env. variable that the OS sets for the specific 
user environment 
    printenv | less 

printenv USER - prints a specific env. variable OR
echo $USER 

Use Case: Sensitive data for application
DB_PWD=secretpassword
DB_USER=mysqluser
    These data can be set as env variable on server which then make them
    available in the user environment
```

<h3> Creating Env. Variables </h3>

```console
Define the variable name on the CLI
    export DB_USERNAME=dbuser
    export DB_PASSWORD=secretpwdvalue
    export DB_NAME=mydb
    -printenv | grep DB
```

<h3> Deleting Env. Variable </h3>

```console
unset [nameofthevariable]
    -unset DB_NAME
```

<h3> Persisting Env. Variable per user </h3>

```console
.bashrc: is a shell specific configuration file per user
         holds the environment variables specific to the user

1. vi into .basharc
     export DB_USERNAME=dbuser                                                    export DB_PASSWORD=secretpwdvalue                                     
     export DB_NAME=mydb 
wq! THEN 
2. source .bashrc
    -this loads the new env. vars into the current shell session
```

<h3> Persisting Env. Variable System Wide </h3>

```console 
1. vi into the file 
    -vi/vim '/etc/environment'

2. export the variable here and save
```


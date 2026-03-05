<h1> Intro to Shell Scripting </h1>

```console 
-Avoid repetitive work
-Keep history of configuration
-Share the instructions 
-Logic & bulk operations 

Shell Scripts have a '.sh' file extension 
What is Shell? the program that interprets and executes the various commands that we type in the terminal 
               Translates our command so that the OS kernel can understand it 

Different Shell Implementations 
1. sh (Bourne Shell) - /bin/sh 

2. Bash (Bourne again shell) - /bin/bash
    default for most Linux systems 
    improved version of sh 
```

<h3> Creating a Script </h3>

```console 
1. Write a Shebang line which tells the OS which shell to use
    -basically saying use SH, BASH, or ZSH shell
    
    -vi setup.sh
    #!/bin/bash: declaration of bash shell 

2. Write & execute a simple script 
    #!/bin/bash

    echo "Setup and configure server"

3. Execute it 
    - ./setup.sh (univeral way of executing a script)
    - bash setup.sh (BASH specific)
```


<h1> Varaibles: Shell Scripting Part 2 </h1>

<h3> Variables </h3>
```console 
Variables: used to store data and can be referenced later
similar to variables in general programming languages 

varaible_name=value assigns the value to the variable
    -no spaces around the = sign

variable_name=$(command): store output of a command in a variable 

#!/bin/bash 

LOG_DIR="/Users/nana/logs"
APP_LOG_FILE="application.log"
SYS_LOG="system.log"

LOG_DIR=variable name 
Variables are noted by $LOG_DIR
```

<h3> Arrays </h3>

```console 
Arrays are Zero-indexed meaning 
-the first element is at index 0
-second element is at index 1 
-and so on 
Ex: 
ERROR_PATTERNS=("ERROR" "FATAL" "CRITICAL")

Arrays are denoted by ${[]}
    so "${[ERROR_PATTERNS[0]}"

Array variables are denoted by 
        ${[@]}: subscript that means "each element remains a separate entity"
        ${[*]}: expands all elements as one big string 
```

<h3> Command Substitution </h3>

```console 
LOG_FILES=$(captured-value)
echo "$LOG_FILES"
```

<h3> Loops </h3>

```console 
Loops are used to repeat a set of commands multiple times-either for a fixed 
number of times. or for every item in a list (like a file, array, or command output)
Syntax:
for 
done 


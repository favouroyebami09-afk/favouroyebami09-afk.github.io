<h1> Linux Basic Commands </h1>

<h3> Use of Pipe & Less </h3>

```console 
ls /usr/bin: this prints a lot into command line, HOWEVER, 
ls /usr/bin | less : gives page by page view of the directory content 
    -hit the 'SPACE' bar for next page
    -press 'b' for previous page 

history 
history | less 
```

<h3> Pipe & Grep </h3>

```console 
grep: globally search for regular expression and print out 
      searches for a particular pattern of characters and displays all lines that contain that pattern 
      ex: history | grep sudo 

Search multiple words with grep and utilization of less again
    -history | grep "sudo chmodo"
    -history | grep sudo | less 
```

<h3> Utilization of redirection </h3>

```console 
Redirection is noted by '>'
    it takes the output from the previous command and sends it to a file that you give 
Ex:
history | grep sudo > sudo-commands.txt
    -it redirect the content of grep sudo into a file named sudo-commands.txt

">>" means append text to end of file 
    simpy means add new stuff to the file w/o deleting the existing file contents 
    -history | grep rm >> sudo-rm-commands.txt


Bonus: You can execute commands independent from each other w/o sharing output and input streams 
    -clear; sleep1; echo "Hope you are enjoying the lecture"
    -independently executed commands 
```

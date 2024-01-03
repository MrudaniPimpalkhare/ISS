
1. Bash - referred to as a shell in the industry
2. Enter commands, result - output

## Commands

1. ls - list storage : lists storage of the current working directory
2. cd ~ : goes to the home directory (cd -- change directory)
3. echo : prints
4. $SHELL : stores the name of the shell you are using within the terminal. The default is /bin/bash (for Linux)

## bash script

a text file that just lists the commands in the form of a script
when this script is executed, the commands are too, one by one.
once you write a bash script in a file, you need to mark it as executable
this is done by the chmod command.
`chmod +x myscript.sh`

- needs to be done using `sudo`  authentication/ by logging in as root
(executable bash script files are seen in green when you execute ls)

the .sh suffix is not necessary to create a bash script. It's a mere convention.
What sets other bash script files apart from other files is the below text:

```
#!bin\bash
ls
pwd
```

execute using the command ./(filename)
```
mrudani@mrudani-OMEN-by-HP-Laptop-16-b1xxx:~$ ./myscript.sh
```

output:
```
Desktop  Documents  Downloads  helloworld.sh  Music  myscript.sh  Pictures  Public  snap  Templates  Videos
/home/mrudani
```
- shebang - tells the script which interpreter it's supposed to use
- rest of the lines written starting with a `#` are treated as comments.
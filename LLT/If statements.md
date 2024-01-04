```
#!/bin/bash
mynum=200
if[mynum -eq 200]
then 
	echo "true"
fi
```

1. -eq : equivalence condition, -ne : not equal condition
2. fi: denotes hat the if statement has ended, the interpreter can move on to the next command
3. else condition: straightforward, make sure you end it with a fi
4. -gt : greater than 
5. -f : checks whether a file exists or not

```
if [-f ~/myfile]
then
	echo "file exists"
else
	echo "lmao no"
fi
```

6. `touch`  : creates file
7. `rm` remove

8. `sudo apt update`
The sudo apt update command is **used to download or refresh the local package index and to provide the system with the most recent information about available packages from the repositories**.

9. `command -v`  is a *command* that  checks whether a command exist
the square brackets are used in the if statements if the format is test
`man test` and find out more

if not, for instance, `command -v` which is a command by itself, the test format isn't executed. The if is true if the particular command exists

for example:

```
if command -v htop
#true

if command -v lmao
#false
```


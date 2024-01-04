*be careful about spaces*

variables can be declared in the Command Line or in a script

```
mrudani@mrudani-OMEN-by-HP-Laptop-16-b1xxx:~$ myname="Mrudani"
mrudani@mrudani-OMEN-by-HP-Laptop-16-b1xxx:~$ echo $myname

```

use a dollar sign whenever you reference a variable in bash.
 if you try to "echo" a variable that hasn't been declared yet, it's treated as an empty variable.
 
```
mrudani@mrudani-OMEN-by-HP-Laptop-16-b1xxx:~$ ls="LMAO"
mrudani@mrudani-OMEN-by-HP-Laptop-16-b1xxx:~$ echo ls
mrudani@mrudani-OMEN-by-HP-Laptop-16-b1xxx:~$ ls
mrudani@mrudani-OMEN-by-HP-Laptop-16-b1xxx:~$ echo $ls

output:
1. ls
2. lists storage
3. LMAO
```

the command `exit` exits the window
 any variable declared in bash is valid only for that session.
 Variable don't persists by default.

- Variables declared in bash scripts persist.
- Helps avoid retyping, increases efficiency.


### Using the output of a command within a bash script

You could also store an output in a variable
```
mrudani@mrudani-OMEN-by-HP-Laptop-16-b1xxx:~$ files=$(ls)
mrudani@mrudani-OMEN-by-HP-Laptop-16-b1xxx:~$ echo $files
```

this is different from saying ```
```
files=$ls
```
(empty variable)

1. date command
2. system/environment variables(commonly in all caps): built in , eg. ```$USER```
3. good practice to use variables in lowercase, for convenience
4. the `env` command gives you the list of all built in variables


## Basic Math

1. the evaluate expression command `expr` evaluates
eg.
```
mrudani@mrudani-OMEN-by-HP-Laptop-16-b1xxx:~$ expr 30+10
mrudani@mrudani-OMEN-by-HP-Laptop-16-b1xxx:~$ expr 10 - 10
```

2. multiplication in bash
```
mrudani@mrudani-OMEN-by-HP-Laptop-16-b1xxx:~$ expr 100 * 4
expr: syntax error: unexpected argument ‘Desktop’
```

-- * is a wildcard symbol. It means everything, i.e running the command against everything in the directory.
While running the command, it ran into Desktop first(alphabetically), hence gave the error referring to desktop.

-- escape out the asterisk, using `\` : useful if you might have accidentally used a symbol used for some other purpose

```
mrudani@mrudani-OMEN-by-HP-Laptop-16-b1xxx:~$ expr 100 \* 4
expr: syntax error: unexpected argument ‘Desktop’

```



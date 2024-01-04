
1. `ls -F`  to not only list the directories within the current directory, but to also label which ones are files and which ones are folders(using color code).
		- / indicates a directory
		- @ : link
		- * indicates an executable
2. `ls -l` also prints the author of each file
3. `ls -l [FILENAME/DIRECTORY NAME]`  lists the files in the required directory

4. the `alias` command: some commands are really hard to type, especially when they are going to be used again and again, and the directory names are considerably long. In that case, the `alias` command gives you a shortcut
		- `alias (alias name) "command_name"`
		- unaliasing `unalias [alias name]`
		- `alias-p` option prints all the defined aliases 

5. `cd ..` moves you up one directory level
6. `cd -` moves you to previous directory that you were in
7. `ls-s` displays size alongside the names
8. `ls -S` sorts the directories by size

### General syntax of a shell command

`$ ls -F /`

*prompt command option argument* (pcoa)


### More commands

1. `mkdir` creates a directory for you
2. `touch [FILENAME]` makes a file.
3. `mkdir -p` allows you to create a directory with nested sub-directories in a single operation.
4. `ls -R` lists all nested sub-directories within a directory
5. `ls - FR` lists nested directories in a recursive order 

### Copying, Moving files and directories

1. `mv`  : short for move. Used for both moving a file or renaming it
```
	mv [options(s)] [source_file_name(s)] [Destination_file_name]
```

source: name of the files that we want to rename or move
destination: name of the new location/ file.

2. `cp` copies a file instead of moving it. 
3. `cp -r`  copies a directory and all it's contents (backing up)
		if you want to copy/backup a directory, the `-r` option is mandatory. If you don't include this option, you'll face an error `-r not specified`

4. `mv file.txt .`
	the file will be transferred to the directory you are currently working on.


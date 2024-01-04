
combining existing programs in different ways

1. `wc` : word count : returns three values, the number of lines, words and characters in the file
2. `wc -l` : outputs only the number of lines, `-m` : number of characters, `-w` : number of words
3. `>` redirects the command's output to a file instead of printing it to the screen.
	ex. `$ wc -l *.pdb > lengths.txt`

#### Filtering outputs

1. `sort -(option)` sorts the contents of the file
	consider a file containing a list of numbers. If you want to sort these numbers in increasing order, use the option `-n` : describes a numerical sort rather than an alphanumerical sort. **this command does not change the contents of the file**, it just sends the sorted result to the screen.
you could send this sorted output to another files using the `>`  symbol.

*redirecting the output of a command to the same file is usually a bad idea - might lead to unnecessary and unrecoverable modifications*


2. `>>` is similar to the `>` operator, except it appends the string, or the content written to the file, in case the file already exists. `>` will overwrite the contents


3. `head -n (number) [file name]` gets the first (number) lines of the file.

4. Appending data
```
$ head -n 3 animals.csv > animals-subset.csv
$ tail -n 2 animals.csv >> animals-subset.csv
```
 head : appends the first few lines
 tail : appends the last few lines

### Passing the output to another command

say you want to print the first two lines of a sorted output(of some file) on the screen
we use the pipe symbol `|`  to transfer the output as follows:
```
$ sort -n lengths.txt | head -n 1
```

### Combining multiple commands

`$ wc -l *.pdb | sort -n | head -n 1`

output is sorted according the number of lines in each file, and the first line of this output is printed onto the screen.

`$ wc -l` : does nothing, terminal sits there and waits for us to give some kind of input interactively.

![Redirects and Pipes of different commands: "wc -l *.pdb" will direct theoutput to the shell. "wc -l *.pdb > lengths" will direct output to the file"lengths". "wc -l *.pdb | sort -n | head -n 1" will build a pipeline where theoutput of the "wc" command is the input to the "sort" command, the output ofthe "sort" command is the input to the "head" command and the output of the"head" command is directed to the shell](https://swcarpentry.github.io/shell-novice/fig/redirects-and-pipes.svg)
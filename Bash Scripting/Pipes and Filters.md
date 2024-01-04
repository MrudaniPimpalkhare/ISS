
combining existing programs in different ways

1. `wc` : word count : returns three values, the number of lines, words and characters in the file
2. `wc -l` : outputs only the number of lines
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

say you want to print the first two lines of a sorted output(of some file) into another file
instead of writing two separate commands like so:
```
$ sort -n
```

	
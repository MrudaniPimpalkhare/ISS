# Find

For comprehensive file and directory searches within a hierarchical structure.
Allows user to search according to name, size, modification time, content, etc.

```bash
find [path] [options] [expression]
```

1. `path` : starting directory of the search
2. `options` : additional settings for the search
3. `expression` : filtering

### Options

1. `-name pattern` 
2. `-type type` : type of file to search for
3. `-size [+/-]n` : searches based on file size. `+n` : files larger than the size, `-n` : for files smaller than the size.
4. `-mtime n` : modification time, n represents the number of days
5. `-exec command {} \;` : executes a command on each file found.
6. `-print` displays the path names of the files that match the criteria
7. `maxdepth , mindepth` : restricts the depth of the directory search.
8. `-empty` : finds the empty files and directories
9. `-delete` : deletes the matched files
10. `-execdir command {} \;` : executes a command on each file found in the directory.
11. `-iname pattern` : case-sensitive version of name (uppercase and lowercase letters). 

# Tree

```bash
tree [options]
```


## Options

1. `version`
2. `-a or -all` : includes hidden files and directories in the tree
3. `-d` or `-dirs-only` : lists only directories
4. `-f or -full-path` : prints the full path prefix of each file
5. `-i or -ignore-case` : case insensitive while sorting
6. 
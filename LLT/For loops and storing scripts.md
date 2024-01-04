```
#!/bin/bash
for current_num in {1..10}
do
	echo $current_num
	sleep 1
done

echo "this is outside the loop."

```

(basic syntax)

```
#!/bin/bash
for file in logfiles/*.log
do
	tar -czvf $file.tar.gz $file
done
```

iterates over the files in the `logfiles`directory with extension `.log` runs tar command on that file, where the name of the compressed file is `$file.tar.gz` , and the file compressed is the file called `$file` .

- can be used to compress a large amount of files


# Storing scripts

- the home directory isn't the best place to run your scripts from
- why? not easy for other administrators to access


### FHS : the file system hierarchy standard

1. describes the conventions of the layout of linux
2. sudo command is required to modify directories that you don't own, for example `usr/local/bin`

```

```
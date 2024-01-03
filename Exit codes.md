Allow us to determine whether the command was executed successfully.

1. The `$?` represents the exit status of the previous command
2. 0 for a successful command, non-zero otherwise.


## utilizing exit codes

```
#!/bin/bash

package2=htop  #command exists
package=lmao #command does not exist

sudo apt install $package2 #exit code is non zero in this case, 0 if you install package2

#echo "The exit status is" $?

if [ $? -eq 0 ]
then
	echo "The installation of the package was successful, new command available here"
	which $package2

else
	echo "installation failed"

fi

```

- the output would be something like:
```
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
htop is already the newest version (3.2.2-2).
0 upgraded, 0 newly installed, 0 to remove and 55 not upgraded.
The installation of the package was successful, new command available here
/usr/bin/htop

```

if you don't want to see this text on your terminal, it's a good idea to "append" that output to a file.

```
#!/bin/bash

package=htop  #command exists


sudo apt install $package << package_install_results.log

#echo "The exit status is" $?

if [ $? -eq 0 ]
then
	echo "The installation of the package was successful, new command available here"
	which $package2

else
	echo "installation failed"

fi
```

```
directory=/etc
if [ -d $directory] #checks if a file exists and is a directory
then 
	echo "directory exists"
else
	echo "directory does not exist"
fi

echo $?
```

the exit status turns out to be 0.
One first glance this makes sense since /etc is a directory, but the exit status does not represent the existence of the file, it just represents whether the execution of the echo was successful or not.
even if the file doesn't exist, it's successfully echo-ing the required statements, hence the exit code is 0.
*check the exit code at the most appropriate time*
(add `echo $?`  right before the DNE echo)
If you replace /etc with a directory that does not exist in your machine, the exit status is still 0.

`exit 199`  command forces the program to exit with exit code - 199.

```
#!/bin/bash

sudo apt install notexist
exit 19
echo $?
```

output : an error, since there is not software/command called notexist.
but it does not print 19
*reason : the interpreter **exits** the program with code 19*
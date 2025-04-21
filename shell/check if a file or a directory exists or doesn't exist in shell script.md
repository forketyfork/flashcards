START
Basic
Front: 
How to check if a file or directory exists or doesn't exist in a shell script?
Back: 
```sh
# to check if file exists
if [ -f file ]; then
	# do something
fi

# to check if file doesn't exist
if [ ! -f file ]; then
	# do something
fi

# to check if directory exists
if [ -d directory ]; then
	# do something
fi

# to check if any type of file exists (dir, file, symlink, etc)
if [ -e file ]; then
	# do something
fi
```
<!--ID: 1719989843460-->
END

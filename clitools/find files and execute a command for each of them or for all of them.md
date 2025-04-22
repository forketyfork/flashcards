START
Basic
Front: How to find files and execute a command for each of them or for all of them?
Back: 
The following command executes the command `echo "file found" filename` for each found file:  
`find . -type f -exec echo "file found" {} \;`  
The following command executes the echo command only once, providing it the space-separated list of files:  
`find . -type f -exec echo "files found" {} \+`
<!--ID: 1745238713659-->
END

START
Basic
Front: How to find files and execute a command for each of them or for all of them?
Back: 
**Execute command for each file individually:**  
`find . -type f -exec echo "file found" {} \;`  

**Execute command once with all files as arguments:**  
`find . -type f -exec echo "files found" {} \+`  

Key differences:
- `\;` runs the command once per file (similar to a loop)
- `\+` runs the command once with all files passed as arguments (more efficient for operations that can handle multiple files)
<!--ID: 1745238713659-->
END
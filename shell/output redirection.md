START
Basic
Front: How do you redirect the standard output of a command into a file? How to append to this file instead of rewriting it? What is "clobbering" and how to prevent it in bash? What are the command's stream ID 0, 1, and 2? How to send the standard output of a command to standard input of another command? How to redirect standard error of a command into a file? How to redirect it to the same place as standard output? How to channel a file into a program's standard input?
Back: 
- To redirect stdout of a command into file, use the notation `command > file`. By default, the file will be "clobbered", or erased, before writing into it. To prevent this in bash, do `set -C`. To append to a file instead of rewriting, use syntax `command >> file`.
- The Stream ID 0 is stdin, the Stream ID 1 is the stdout, and the Stream ID 2 is the stderr.
- To send the stdout of a command into stdin of another command, use pipe: `command1 | command2`.
- To redirect stderr, use the notation 2> like that: `command > file_out 2> file_err`. 
- To redirect stderr to the same place as stdout, use notation 2>&1: `command > file_out 2>&1` 
- A shorthand for redirecting both streams is `command &> file_out`
- To channel a file into the program's stdin, use < notation: `head < /proc/cpuinfo`
<!--ID: 1708150680084-->
END

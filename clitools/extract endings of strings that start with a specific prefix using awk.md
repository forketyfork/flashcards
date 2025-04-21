START
Basic
Front: How do you extract endings of strings that start with a specific prefix using awk? For instance, for this file:
```
hello, world!
hello, me!
what's going on?
hello, huge dinosaur!
```
It should print:
```
world!
me!
dinosaur!
```
Back: 
`awk '/^hello/{print $NF}' myfile.txt`  

- `/^hello` will find a string that starts with `hello`;
- `{print $NF}` will print out the last field (whitespace-separated word) in this string, `NF` being the total number of the fields.
<!--ID: 1745222709467-->
END

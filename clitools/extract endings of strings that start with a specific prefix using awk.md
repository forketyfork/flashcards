START
Basic
Front: How do you extract endings of strings that start with a specific prefix using awk?
Back: 
`awk '/^Prefix/{print $NF}' myfile.txt`  

- `/^Prefix` will find a string that starts with `Prefix`;
- `{print $NF}` will print out the last field (whitespace-separated word) in this string, `NF` being the total number of the fields.

END

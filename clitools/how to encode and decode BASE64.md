START
Basic
Front: How to encode and decode BASE64 using command line?
Back: 
```sh
> echo -n Hello! | base64
SGVsbG8h
> echo -n SGVsbG8h | base64 -d
Hello!
```
The `-n` parameter of the `echo` command makes sure it doesn't print the terminating newline.
<!--ID: 1745238713615-->
END

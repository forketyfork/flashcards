START
Basic
Front: How do you run the docker login command non-interactively?
Back: 
You can use the `--password-stdin` argument to read the password from `STDIN` instead of providing it as an argument. This will prevent the password from ending up in shell history or log files. As an example, here's how to read the password from a file and pass it to the command:
```sh
cat ~/my_password.txt | docker login --username foo --password-stdin
```
<!--ID: 1745138891616-->
END

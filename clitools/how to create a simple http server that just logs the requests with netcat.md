START
Basic
Front: 
How to create a simple http server that just logs the requests using `netcat`?
Back: 
```sh
nc -l -p 31337 -k
```
Where:
- `-l` — listen instead of connecting to the port;
- `-p` — which port to use (on macOS, you don't need this argument here, just specify the port after the `-l` option);
- `-k` — after the connection is terminated, wait for another connection (only used with the `-l` option).

The incoming requests will be logged to the console.

If you want this server to actually answer 200 OK, you can use the following command, but it won't terminate the output, so the client will most likely hang indefinitely:
```sh
while true; do echo -e "HTTP/1.1 200 OK\n\n $(date)" | nc -l -p 31337; done
```

`echo -e` means that echo will process escape sequences, e.g. `\n`.

END

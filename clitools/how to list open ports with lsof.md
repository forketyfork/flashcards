START
Basic
Front: 
How to list open TCP ports using `lsof`?
Back: 
```sh
lsof -iTCP -sTCP:LISTEN
```

`-i` selects the protocol, `-s` selects protocol state.
<!--ID: 1745238713571-->
END

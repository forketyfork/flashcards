START
Basic
Front: 
How to list open TCP ports using `lsof`?
Back: 
```sh
lsof -iTCP -sTCP:LISTEN
```

`-i` selects the protocol, `-s` selects protocol state.

END

START
Basic
Front: 
Take a string `251.14886` and make `2025.1` out of it using sed.
Back: 
```shell
echo "251.14886" | sed -r 's/(..)(.*)\..*/20\1.\2/'
```

END

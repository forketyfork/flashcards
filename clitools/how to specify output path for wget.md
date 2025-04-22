START
Basic
Front: How to specify output path or file name for wget?
Back: 
To specify output file name:
```sh
wget <uri> -O /path/to/file.ext
```
To specify just the file output path:
```sh
wget <url> -P /path/to/
```

`-O`, or `--output-document`, defines the full file path, while `-P`, or `--directory-prefix`, specifies just the directory.
<!--ID: 1745238713554-->
END

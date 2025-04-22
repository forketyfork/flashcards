START
Basic
Front: 
How to compress a PDF using Ghostscript (preserve text and vectors)?
Back: 
```shell
gs -sDEVICE=pdfwrite \
   -dCompatibilityLevel=1.4 \
   -dPDFSETTINGS=/screen \
   -dNOPAUSE \
   -dQUIET \
   -dBATCH \
   -sOutputFile=output.pdf \
   input.pdf
```

- `-s` for string parameters, `-d` for numbers and booleans;
- use `/screen`, `/ebook`, or `/printer` for different compression levels, from the highest to the lowest;
- `NOPAUSE` — no pause between page renders;
- `QUIET` — suppresses most terminal output;
- `BATCH` — prevents Ghostscript from prompting you when done;
<!--ID: 1745299611388-->
END
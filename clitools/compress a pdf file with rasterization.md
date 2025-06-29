START
Basic
Front: How to compress a PDF file using imagemagick (with page rasterization)?
Back: 
```
convert -density 300 -quality 80 -compress jpeg original.pdf output.pdf
```

This rasterizes each page at 300 DPI and compresses it as JPEG. 

Use with caution—this strips text and vector data. Prefer `gs` for better PDF compression when you want to keep searchable text.
<!--ID: 1745299611387-->
END

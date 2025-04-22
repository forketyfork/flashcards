START
Basic
Front: How to copy data from `Reader` to `Writer` in Go?
Back: 
You can use the `io.Copy` function: `func Copy(dst Writer, src Reader) (written int64, err error)`.
It copies from `src` to `dst` until either `EOF` is reached on `src` or an error occurs, returning the number of bytes copied and the first error encountered while copying, if any. A successful `Copy` returns `err == nil`.
If `src` implements `WriterTo`, then the copy is implemented by calling `src.WriteTo(dst)`; otherwise, if `dst` implements `ReaderFrom`, copy is implemented by calling `dst.ReadFrom(src)`.
<!--ID: 1745299611376-->
END

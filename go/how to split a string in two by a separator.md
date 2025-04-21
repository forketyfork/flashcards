START
Basic
Front: 
How do you split a string in two by a separator?
Back: 
If you just need to split a string in two, use the `strings.Cut` function to split a string `s` around a separator `sep`. It will return strings before and after a separator and `true`.
```go
func Cut(s, sep string) (before, after string, found bool)
```
If the separator is not found, it will return `s, "", false`.
<!--ID: 1745139558105-->
END

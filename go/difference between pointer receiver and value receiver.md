START
Basic
Front: 
What's the difference between a pointer receiver and a value receiver of a function?
Back: 
A pointer receiver, e.g. `func (v Vertex) Abs()`, means that we're operating on a value copy, and any modifications to the receiver will be done on a value copy:
```go
func (v Vertex) Scale(f float64) {
	v.X = v.X * f
	v.Y = v.Y * f
}

func main() {
    // this is most likely an error, as it won't affect v
	v.Scale(10)
}
```

To allow the function to modify the receiver, use the pointer receiver: `func (v *Vertex) Scale()`.
<!--ID: 1745139558113-->
END

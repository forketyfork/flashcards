START
Basic
Front: How do you get a directory of a file in Go? Describe the corresponding function.
Back: 
You can use the `func Dir(path string) string` function from the `filepath` package as follows.
`Dir` returns all but the last element of path, typically the path's directory. After dropping the final element, `Dir` calls `Clean` on the path and trailing slashes are removed. If the path is empty, `Dir` returns `"."`. If the path consists entirely of separators, `Dir` returns a single separator. The returned path does not end in a separator unless it is the root directory.

Examples of conversion for Unix:
```
"/foo/bar/baz.js" -> "/foo/bar"
"/foo/bar/baz" -> "/foo/bar"
"/foo/bar/baz/" -> "/foo/bar/baz"
"/dirty//path///" -> "/dirty/path"
"dev.txt" -> "."
"../todo.txt" -> ".."
".." -> "."
"." -> "."
"/" -> "/"
"" -> "."
```
<!--ID: 1745139558108-->
END
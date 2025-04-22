START
Basic
Front: How do you execute a program in Go and replace the currently running process with it?
Back: 
Use the `syscall.Exec` system call which calls `execve(2)`: `func Exec(argv0 string, argv []string, envv []string) (err error)`

It executes the program referred to by `argv0` which is (by convention) the same as `argv[0]`. This causes the program that's currently being run by the calling process to be replaced with a new program, with newly initialized stack, heap, and (initialized and uninintialized) data segments.
<!--ID: 1745299611375-->
END

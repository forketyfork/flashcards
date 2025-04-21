START
Basic
Front: How is the current directory handled in the exec package functions like `LookPath` and `Command`? Why? How to work around this behavior?
Back: 
Due to security reasons, starting from Go 1.19, the current directory is always excluded from the `Command().Run()` and `LookPath` function search path, regardless of how the `PATH` directory is configured. Those functions will return an error satisfying `errors.Is(err, ErrDot)`.
You can work around this by:
- specifying the `./execname` path
- clearing the `error` returned by the functions;
- disabling the generation of `ErrDot` entirely by setting the env variable `GODEBUG=execerrdot=0`
<!--ID: 1745139558114-->
END

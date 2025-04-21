START
Basic
Front: Describe a Go function for finding an executable in PATH
Back: 
`func LookPath(file string) (string, error)`
Searches for an executable in `PATH`. If `file` contains a slash, it's tried directly, and the PATH is not consulted; otherwise, on success, the result is an absolute path. Before Go 1.19, could return a path relative to the current directory; now will instead return that path along with an error satisfying `errors.Is(err, ErrDot)`.

END

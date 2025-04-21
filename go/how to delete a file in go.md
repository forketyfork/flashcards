START
Basic
Front: How to delete a file in Go? How to check if it was really deleted or just absent?
Back: use `os.Remove(name string) error`. It removes the named file or (empty) directory. If there is an error, it will be of type `*PathError`. You can use `os.IsNotExist(err)` function to check the returned error, `true` would mean that the file didn't exist in the first place.
<!--ID: 1745139558109-->
END

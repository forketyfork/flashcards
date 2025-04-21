START
Basic
Front: Where is Go module cache located, and how to clean it?
Back: See `~/go/pkg/mod` and `~/go/pkg/mod/cache`. To clean the cache, run `go clean -modcache`. It will remove the entire module download cache, including unpacked source code of versioned dependencies.
<!--ID: 1745139558100-->
END

START
Basic
Front: 
Write a minimal web server in Go that listens to localhost:8080 and just outputs "Hello" for every request. Test it using curl.
Back: 
```go
package main

import (
	"fmt"
	"net/http"
)

func hello (w http.ResponseWriter, _ *http.Request) {
	fmt.Fprintf(w, "Hello")
}

func main() {
	http.HandleFunc("/", hello)
	err := http.ListenAndServe("0.0.0.0:8080", nil)
	if err != nil {
        fmt.Printf("Error: %v\n", err)
	}
}
```

To run it:

```sh
go run web-server.go
```

To test it:

```sh
curl localhost:8080 -vvv
```
<!--ID: 1745139558102-->
END

START
Basic
Front: 
How do you unmarshal JSON and fail on unknown fields?
Back: 
Some imports first:
```go
package main

import (
	"encoding/json"
	"strings"
	"fmt"
)
```
You can define an object like this:
```go
type MyObject struct {
	MyProperty string `json:"myProperty"`
}
```
And then parse it like this:
```go
func main() {
	myJsonString := `{"myProperty":"Hello World"}`
	
	myObject := &MyObject{}
	decoder := json.NewDecoder(strings.NewReader(myJsonString))
	// or use bytes.NewReader(myJsonBytes) for bytes
	decoder.DisallowUnknownFields()
	decoder.Decode(&myObject)
	
	fmt.Println(myObject.MyProperty)
}
```
<!--ID: 1745139558104-->
END

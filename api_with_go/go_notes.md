# README

Author: Lin Dong

Date: Mon Apr 20 09:21:39 PDT 2015

##Go Playground

Download via `git clone https://github.com/ArdanStudios/gotraining`

### Build-in type

```go
package main

import fmt

func main(){
// declare and assign to its default value
  var a int
  var b string
  var c float64
  var d bool
}

aa := 10
bb := "hello"
cc := 3.1415
dd := false
```

`var` will assign it to 0 value

`int` is architecture specific.

`string` is immutable.

### Struct

size and representation

### Anonymous Struct

```go
e := struct {
  flag bool
  counter int16
  pi float32
}{
  flag: true,
  counter: 10,
  pi: 3.1415
}
```

### Pointer

Pointer type, thinking about `sharing`

Reserve the pointer to share

pass by value, composite literal

``` go
type user struct {
  name string
  email string
  gender string
}
```

### Slices

`Mechanical Sympathy` to write in a way that helps Machine to predict

```
slice := make([]string, 5)
slice[0] = "Apple"
slice[1] = "Apple"
slice[2] = "Apple"
slice[3] = "Apple"
slice[4] = "Apple"
```

`Slice` just like an dynamic growing `array`

```
make()
append()
cap()
len()
```

### HTTP Router API

See in folder **12-http**

Using `func` to declare function.

```go
func(){}

// anonymous function
go function(){}
```

### Tips

Using logs more often than debugs

Using environment variable


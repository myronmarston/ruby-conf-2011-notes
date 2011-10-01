## Go <=> Ruby

* Google Go: it's not just for google
* There's a language spec that's being implemented for Go.
* Ruby typing is tricksy:
  * Expressed type: intersection of instance class, inherited class modules
* type in Go is safe 
  * clearly defined areas of doubt and uncertainty
  * static type is intersection of memory layout, method set, and embedded types
  * slice: an immutable array
  * interface: a set of methods. Any type that has them can be an
    instance of it, without having to declare it like in java.
  * types are fixed at compile time
* No REPL for go
* go test--a testing tool for go
  * built in benchmarking
* go doesn't have exceptions
* go has closures
  * it also has "defer"--which will run the closure as it unwinds the stack
* for is the only loop construct in go
* no generics--but some generic functions are coming
* `go func`--a go routine. moves to a separate thread when it blocks on IO.
* go channels are like unix pipes

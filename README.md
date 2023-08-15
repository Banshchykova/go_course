##### *GoLang: The complete Developer's Guide* #####

* Introduction
1. Go is an open source programming language that Google developed. Software developers use Go in an array 
of operating systems and frameworks to develop web applications, cloud and networking services, and other types of software.
Go is statically typed, explicit and modeled after the C programming language. Because of Go language's fast startup time, 
low runtime overhead and ability to run without a virtual machine (VM), it has become a very popular language 
for writing microservices and other uses. In addition, Go is used for concurrent programming -- a strategy 
to execute multiple tasks at one time, out of order or in partial order.
Go language was inspired by the productivity and relative simplicity of Python. It uses goroutines, 
or lightweight processes, and a collection of packages for efficient dependency management. 
It was designed to solve several problems, including slow build time, uncontrolled dependencies, effort duplication, 
difficulty writing automatic tools and cross-language development.
2. Package is the collection of common source files.
2. Type of packages: executable(main.go) & reusable(logic or helper functions, dependencies).
3. Import is used to give our package. *Fmt* is the name of a standard library package that is included 
with the go programming language by default.
4. Array vs Slice. Slice is array but more fancy. Both should have the same type of data. 
5. Receiver in Go is a special parameter in a method declaration that allows a type to define methods that can be called 
on its instances. 

* Project "cards"
1. Create *main.go* & *deck.go*
2. Run 
> go run main.go deck.go
3. Test
* before start to test need to run 
> go mod init <go_course> // <go_course>the name of working dir.
* then run
> go test

* Structs
1. Pointer operations
> &variable - give the memory address of the value this variable in a pointing at
> *pointer - give me the value this memory address is a pointing at
Example:
```go
package main

import "fmt"

type contactInfo struct {
	email   string
	zipCode int
}
type person struct {
	firstName string
	lastName  string
	contactInfo
}

func main() {
	jim := person{
		firstName: "Jim",
		lastName:  "Party",
		contactInfo: contactInfo{
			email:   "jim@gmail.com",
			zipCode: 0070707,
		},
	}
	jimPointer := &jim
	jimPointer.updateName("jimmy")
	jim.print()
}

func (pointerToPerson *person) updateName(newFirstName string) {
	(*pointerToPerson).firstName = newFirstName
}
func (p person) print() {
	fmt.Printf("%+v", p)
}
```
* Maps
# Map is a collection of key value pairs.
Maps is that both the keys and the values are statically typed.
So whenever we add some number of keys to a map and go, they must all be of the same exact type.
And then all the different values that we add as well must also be of the exact same type.
Now the keys and the values themselves don't have to be of the same type, just all the different values
have to.

* Diff Structs & Maps
|   Struct                            |   Map
|:----------:                         |------------------
| 1. Values can be of different type  | 1. All values must be the same type. All keys must be the same type
| 2. Value type  | 2. Reference type
| 3. Keys don't support indexing | 3. Keys are indexed - we can iterate over them
| 4. You need to know all the different fields at compile time | 4. Don't need to know all the keys at compile time
| 5. Use to represent a "thing" with a lot of different properties | 5. USe the represent a collection of related properties



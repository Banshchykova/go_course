##### GoLang: The complete Developer's Guide #####
### *INTRODUCTION* ###
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

### *NEW PROJECT* ###
1. Create *main.go* & *deck.go*
2. Run 
> go run main.go deck.go
3. Test
~ Before start to test need to run 
> go mod init <go_course> // <go_course>the name of working dir
then
> go test
4. Test file IO



Slices are an important data type in Go, giving a more powerful interface to sequences than arrays.

Unlike arrays, slices are typed only by the elements they contain (not the number of elements). An uninitialized slice equals to nil and has length 0.

var s []string

To create a slice with non-zero length, use the builtin make. Here we make a slice of strings of length 3 (initially zero-valued). By default a new slice’s capacity is equal to its length; if we know the slice is going to grow ahead of time, it’s possible to pass a capacity explicitly as an additional parameter to make.


s = make([]string, 3)

In addition to these basic operations, slices support several more that make them richer than arrays. One is the builtin append, which returns a slice containing one or more new values. Note that we need to accept a return value from append as we may get a new slice value.
s = append(s, "d")
s = append(s, "e", "f")
    
Slices can also be copy’d. Here we create an empty slice c of the same length as s and copy into c from s.

c := make([]string, len(s))
    copy(c, s)
    fmt.Println("cpy:", c)


Slices support a “slice” operator with the syntax slice[low:high]. For example, this gets a slice of the elements s[2], s[3], and s[4].    
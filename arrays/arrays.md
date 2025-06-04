
In Go, an array is a numbered sequence of elements of a specific length. In typical Go code, slices are much more common; arrays are useful in some special scenarios.

Here we create an array a that will hold exactly 5 ints. The type of elements and length are both part of the array’s type. By default an array is zero-valued, which for ints means 0s.

var abc[5]  string 

The builtin len returns the length of an array.
fmt.Println("len:", len(a))


Use this syntax to declare and initialize an array in one line.
b := [5]int{1, 2, 3, 4, 5}

You can also have the compiler count the number of elements for you with ...
b = [...]int{1, 2, 3, 4, 5}


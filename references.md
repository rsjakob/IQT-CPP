# References

---

A reference can be thought of as a constant pointer \(not to be confused with a pointer to a constant value!\) with automatic indirection, i.e. the compiler will apply the **\*** operator for you.

References are pointers that cannot be null, and you interact with references without having to use the dereference operator.

A reference variable is an alias, that is, another name for an already existing variable. A reference, like a pointer is also implemented by storing the address of an object.

* References can assigned only once
* References will always refer to an initialized object
* You cannot obtain the address of a reference
* There is no such thing as reference arithmetic

> struct Point{
>
> int x, y;
>
> };
>
> voidset\_to\_origin\(Point &point\){
>
> point.x = 0;
>
> point.y = 0;
>
> }
>
> …

---

A pointer is a variable that holds the memory address of another variable. A pointer needs to be dereferenced with **\*** operator to access the memory location it points to.

* Pointers can be reassigned any number of times
* Pointers can point to nothing
* You can obtain the address of a pointer
* Pointer arithmetic is a real thing

> struct Point{
>
> int x, y;
>
> };
>
> void set\_to\_origin\(Point \*point\){
>
> point-&gt;x = 0;
>
> point-&gt;y = 0;
>
> }
>
> …

---


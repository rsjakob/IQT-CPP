# Templates

---

* Templates are how C++ programmers can do generic programming.
* Generic programming means writing data structures and algorithms without regards for a specific type.
* Templates are very powerful, but can be complicated to write. However, they are easy to use.

> ##### //Don’t do this
>
> ##### int IntegerDataStructure::next\(\);
>
> ##### string StringDataStructure::next\(\);
>
> ##### Foo FooDataStructure::next\(\);
>
> ##### 
>
> ##### //Do this instead
>
> ##### T DataStructure&lt;T&gt;::next\(\);

---


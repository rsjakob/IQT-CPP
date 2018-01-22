# C++ Standard Template Library

---

* Don’t work harder than you have to
* The STL probably has a cleaner solution than your custom made one
* When programming, try and find a solution that is in the STL.
* If you need a data structure, there is probably already a container in the STL
* If writing a common algorithmic task, there is probably already a generic version of it in the STL \(think counting, searching, replacing, finding\)

#### Containers

* **Strings: **length, substr, find, append, operator\[\], data, c\_str
* **Vectors: **operator\[\], front, back, data, emplace\_back, empty, clear
* **Maps:** emplace, operator\[\], at, erase

**Streams:** cin, cout, ofstream, ifstream

**Templates:** using generic types with the STL.

**Iterators:** range based for loops, flavors, begin, end, back\_inserter

**Algorithms:** erase, remove, accumulate, iota, find, copy, transform, replce, sort

**Lambdas:** using anonymous functions.

> ##### int g\(int a\[\],int l,int r\) {
>
> #####     int pivot, i, j, t;
>
> #####     pivot = a\[l\];
>
> #####     i= l; j = r + 1;
>
> #####     while\(true\) {
>
> #####         do ++i, while\(a\[i\] &lt;= pivot && i &lt;= r\);
>
> #####         do --j, while\(a\[j\] &gt; pivot\);
>
> #####         if\(i&gt;= j\) break;
>
> #####         t = a\[i\]; a\[i\] = a\[j\]; a\[j\] = t;
>
> #####     }
>
> #####     t = a\[l\]; a\[l\] = a\[j\]; a\[j\] = t;
>
> #####     return j;
>
> ##### }




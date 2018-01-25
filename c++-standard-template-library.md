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

---

![](/assets/30.PNG)

![](/assets/31.PNG)

---

If you use the std::sort, it's clear what you are doing.

Writing your own common algorithm makes your code obscure, more error-prone, and a waste of time.

Use the STL!

> #### vector&lt;int&gt; a\({2, 8, 5, 6, 1, 1, 0}\);
>
> #### sort\(a.begin\(\), a.end\(\)\);

---


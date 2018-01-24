# STL Iterators

---

Iterators are fundamental building blocks of the STL. They connect **containers **to _algorithms_.

All STL containers have **begin\(\)** and **end\(\)** methods that return iterators.

They are like _pointers_, but a bit safer to use.

> ##### vector&lt;int&gt; fibonacci{0, 1, 1, 2, 3, 5, 8};
>
> ##### auto fib\_iterator = fibonacci.begin\(\);
>
> ##### \*fib\_iterator= 1;
>
> ##### ++fib\_iterator;
>
> ##### REQUIRE\(fibonacci\[0\] == 1\);
>
> ##### REQUIRE\(\*fib\_iterator == 1\);

* **Operator\* ** - returns the element at the current position.
* **Operator++**  - returns the iterator step forward to the next element. Most iterators will let you step backwards with **–**.
* Operator **== ** and operator **!= **return whether or not two iterators represent the same position.
* Operator ** = **  assigns an iterator.

---

Any object that has **begin\(\) ** and **end\(\) ** that return iterators can have a new way to for-loop.

A _range-based_ _for loop _ can use an iterator to loop over the contents of a ** vector**, **map**, or similar STL container.

> ##### vector&lt;int&gt; fibonacci{0, 1, 1, 2, 3, 5, 8};
>
> ##### auto fib\_sum = 0;
>
> ##### 
>
> ##### //range based
>
> ##### for\(const auto& fib\_num: fibonacci\)
>
> ##### {
>
> ##### fib\_sum += fib\_num;
>
> ##### }
>
> ##### 
>
> ##### //regular for loop
>
> ##### for\(auto iterator = fibonacci.begin\(\);
>
> ##### iterator != fibonacci.end\(\); iterator++\)
>
> ##### {
>
> ##### fib\_sum += iterator;
>
> ##### }

| Category | Ability | Example |
| :---: | :---: | :---: |
| Input | Read forward | istream |
| Output | Write forward | ostream, back\_inserter |
| Forward | Read/Write forward | list, set, map |
| Bidirectional | Read/Write forward/backward | list, set, map |
| Random Access | Read/Write & Random Access | vector, string |

Some iterators are already familiar, but notice that **lists **and **maps** can move in either direction.

**Vectors **and **strings **can be accessed randomly from any element within its bounds.


# STL Algorithms

---

#### remove\(\)

**remove\(ForwardIterator first, ForwardIterator last, const T& val\)**

* Removes elements by pushing them to the end of the structure’s range and returning an** iterator **to the last element unchanged;
* Does not actually delete them.
* **remove\(\) ** requires a forward iterator.

> ##### vector&lt;int&gt; fibonacci{0, 1, 1, 2, 3, 5, 8};
>
> ##### auto new\_end = remove\(fibonacci.begin\(\), fibonacci.remove\(\), 1\);
>
> ##### REQUIRE\(fibonacci == vector&lt;int&gt;\({0, 2, 3, 5, 8}\)\);

---

#### **accumulate\(\)**

**accumulate\(InputIterator first, InputIterator last, T init\)**

* Returns the result of summing the elements of the range.
* The third argument is the starting value of the sum.

###### Note: other overloads of this function exist

> ##### vector&lt;int&gt; fibonacci{0, 1, 1, 2, 3, 5, 8};
>
> ##### auto sum = accumulate\(fibonacci.begin\(\), fibonacci.end\(\), 0\);
>
> ##### REQUIRE\(sum == 13\);
>
> ##### fibonacci.insert\(fibonacci.end\(\), sum\);

---

#### erase\(\)/remove\(\) idiom

Recall that **remove\(\) **does not actually delete elements of a container, just pushes them to the end. It is an STL algorithm

**erase\(const\_iterator first, const\_iterator last\)**

**erase\(\) ** actually destructs the elements and resizes the container. It is a method of an STL container.

The two methods form the erase – remove idiom. Finding elements to remove is generic across various containers, but erase is reliant upon how the underlying container manages memory.

> ##### vector&lt;int&gt; fibonacci{0, 1, 1, 2, 3, 5, 8};
>
> ##### fibonacci.erase\(remove\(fibonacci.begin\(\), fibonacci.end\(\), 1\), fibonacci.end\(\)\);
>
> ##### REQUIRE\(fibonacci == vector&lt;int&gt;\({0, 2, 3, 5, 8}\)\);

---

#### iota\(\)

**iota\(ForwardIterator first, ForwardIterator last, T Value\)**

* assigns values in a container matching the old\_value to the new value.
* Returns no value

> ##### vector&lt;int&gt; fibonacci{0, 1, 1, 2, 3, 5, 8};
>
> ##### iota\(fibonacci.begin\(\), fibonacci.end\(\), 0\);
>
> ##### REQUIRE\(fibonacci == vector&lt;int&gt;\({0,0,0,0,0,0,0}\)\);

---

#### replace\(\)

**replace\(ForwardIterator first, ForwardIterator last, const T& old\_value, const T& new\_value\)**

Assigns **new\_value **to all elements in the range **\[first, last\] **that compare equal to **old\_value.**

> ##### vector&lt;int&gt; numbers\(6\);
>
> ##### iota\(fibonacci.begin\(\), fibonacci.end\(\), 42\);
>
> ##### numbers\[1\] = 18;
>
> ##### numbers\[3\] = 36;
>
> ##### numbers\[5\] = 54;
>
> ##### replace\(numbers.begin\(\), numbers.end\(\); 18, 76\);
>
> ##### REQUIRE\(numbers == vector&lt;int&gt;\({42, 76, 42, 36, 42, 54, 42}\)\);

---

#### sort\(\)

sort\(RandomAccessIterator first, RandomAccessIterator last\);

Sorts the elements in the range specified by the _iterator_ parameters with operator **&lt; **\(by default\).

###### Note: Optional parameter exists, third parameter is a function or object that implements a bool comparison.

> ##### boolcomp\_func\(inti, intj\)
>
> ##### {
>
> #####  return\(i&gt;j\);
>
> ##### }
>
> ##### vector&lt;int&gt; numbers\({44, 77, 3, 33, 5, 7, 14, 2}\);
>
> ##### sort\(numbers.begin\(\), numbers.end\(\)\);
>
> ##### REQUIRE\(numbers == vector&lt;int&gt;\({2, 3, 5, 7, 14, 33, 44, 77}\)\);
>
> ##### 
>
> ##### sort\(numbers.begin\(\), numbers.end\(\), comp\_func\);
>
> ##### REQUIRE\(numbers == vector&lt;int&gt;\({77, 44, 33, 14, 7, 5, 3, 1}\)\);

---


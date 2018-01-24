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

returns the result of summing the elements of the range.

The third argument is the starting value of the sum.

###### Note: other overloads of this function exist

> ##### vector&lt;int&gt; fibonacci{0, 1, 1, 2, 3, 5, 8};
>
> ##### auto sum = accumulate\(fibonacci.begin\(\), fibonacci.end\(\), 0\);
>
> ##### REQUIRE\(sum == 13\);
>
> ##### fibonacci.insert\(fibonacci.end\(\), sum\);




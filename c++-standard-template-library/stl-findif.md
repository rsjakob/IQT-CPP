# STL find\_if

---

**find\_if\(InputIterator first, InputIterator last, UnaryPredicate pred\)**

Returns an iterator to the first element in the range** \[first, last\)**, for which the given function returns true.

There is also a **find\_not\_if** function, which returns an iterator to the first element in the range that returns false.

> ##### vector&lt;int&gt; numbers\({2, 4, 5, 6}\);
>
> ##### auto first\_odd = find\_if\(numbers.begin\(\), numbers.end\(\), \[\]\(autonum\){
>
> #####  return num%2 == 1;
>
> #####  }\);
>
> ##### REQUIRE\(first\_odd == numbers.begin\(\) + 2\);

---


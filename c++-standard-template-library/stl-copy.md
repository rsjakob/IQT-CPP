# STL Copy

---

* **copy\(InputIterator first, InputIterator last, OutputIterator result\)**
* Copies the elements in the range **\[first, last\) **into the range beginning at result.
* Returns an iterator to the end of the destination range \(the element following the last element copied\).

> ##### vector&lt;int&gt; source { 1, 2, 3, 4}, destination\(4\);
>
> ##### copy\(source.begin\(\), source.end\(\), destination.begin\(\)\);
>
> ##### 
>
> ##### REQUIRE\(desination == vector&lt;int&gt;\({1, 2, 3, 4}\)\);
>
> ##### 
>
> ##### //Is this potentially unsafe?

---


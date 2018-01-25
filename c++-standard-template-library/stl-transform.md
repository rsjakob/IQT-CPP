# STL transform

---

transform\(InputIterator first1, InputIterator last1, OutputIterator result, UnaryOperation op\) \(unary form\).

Applies a function to the range\(s\) given by the first two \(three if binary\) and assigns the result to the range started by the result argument.

> vector&lt;int&gt; numbers \({4, 0, 2}\);
>
> vector&lt;string&gt; output;
>
> transform\(numbers.begin\(\), numbers.end\(\), back\_inserter\(output\), \[\]\(autolen\)
>
> {
>
>  return string\(len, ‘a’\);
>
> }\);
>
> REQUIRE\(output == vector&lt;string&gt;\({“aaaa”, “”, “aa”}\)\);

---


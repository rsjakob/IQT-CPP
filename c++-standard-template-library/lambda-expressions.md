# Lambda Expressions

---

Lambda expressions are unnamed functions that are written \_inline \_with the rest of your code.

* Also known as anonymous functions.
* Useful for quick functions, where it may be cumbersome to implement a full function or class object.
* Typically used where a _function pointer_ could be used.

> ##### Syntax: \[captured variables\] \(argument list\)
>
> ##### {
>
> ##### //code
>
> ##### }

---

* Lambdas are created with **\[\]**, the capture _clause_.
* This allows the \_lambda function \_to capture a variable from the surrounding scope.
* After the capture clause comes the argument list.
* This example does not capture a variable.
* How is this \_lambda expression \_being used?

> ##### auto fn1 = \[\] \(intx\)
>
> ##### {
>
> ##### return x % 42;
>
> ##### }
>
> ##### REQUIRE\(fn1\(62\) == 20\);

---

* Inside the _capture expression_, we can use the **= **symbol to capture variables from _scope_.
* Variables captured with **= **are captured by _value._
* Multiple captures can be made by separating the values with **,**
* Using **\[=\]** alone will capture all variables from scope. This is not recommended.

> ##### auto divisor = 42;
>
> ##### auto fn2 = \[=divisor\]\(int x\)
>
> ##### {
>
> ##### return x % divisor;
>
> ##### };
>
> ##### divisor = 1; //Does this line matter?
>
> ##### REQUIRE\(fn2\(62\) == 20\);

---

* Lambdas can also capture values by **reference **with the **& **symbol.
* Like with capturing values, you can also use **\[&\]** to capture all scoped references, although this is not recommended.
* Look at the example, and think about the result of the test case at the end.

> auto divisor = 42;
>
> auto fn3 = \[&divisor\]\(int x\)
>
> {
>
> return x % divisor;
>
> };
>
> divisor = 62; //What does this do?
>
> REQUIRE\(fn2\(62\) == 0\);

---


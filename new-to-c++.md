# New to C++

---

#### **We now have'auto'**

###### Usage

* automatic duration storage-class specifier with no linkage.

The **auto **specifier is only allowed for objects declared at block scope \(except function parameter lists\). It indicates automatic storage duration and no linkage, which are the defaults for these kinds of declarations.

* **auto ** lets us specify it once.
* variables declared auto will have the compiler try to deduce what the appropriate data type will be
* As of C++14, auto can also be used as a function return type. This is useful for working with templates, which we cover later.

> \#include &lt;iostream&gt;
>
> int main\(\)
>
> {
>
> ```
>  auto x = 42.0L;
>
>  //code stuffs
>
>  return \(0\);
> ```
>
> }

**auto **can save your life! Or at least your execution:

> \#include &lt;iostream&gt;
>
> int main\(\)
>
> {
>
> ```
> unsigned int bad = -42;
>
> //code stuffs
>
> return \(0\);
> ```
>
> }

---

#### decltype

* **decltype **is useful for trying to deduce a data type, but you do not have an initializer.
* **decltype** extracts the type from another variable.
* Both **auto **and **decltype** are very powerful.

> ##### int foo = 0;
>
> ##### decltype\(foo\) bar;
>
> ##### //bar now has the same type as foo

Allows devs to focus on logic, rather than mundane tasks.

---

#### Runtime Sized Arrays

* New feature to C++14
* Arrays can be sized at runtime.

> void fun\(int i\)
>
> {
>
>     int array\[i\];
>
> }




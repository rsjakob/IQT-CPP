# New to C++

---

#### **We now have 'auto'**

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
> ```
> int array\[i\];
> ```
>
> }

---

#### Functions

You can still use C-style functions:

> ##### int do\_stuff\(int in\_param, char\[\] array, double \*out\_param\)

Major improvements:

* Passing with **references**.
* Passing **structs/classes** by value.
* **const **parameters.

---

#### Default Argument Values

You can make arguments optional by giving them default values:

> ##### double function\_with\_default\(double x=100\)
>
> ##### {
>
> ##### return x;
>
> ##### }
>
> ##### auto a = function\_with\_default\(\);
>
> ##### auto b = function\_with\_default\(42\);

---

#### const

New keyword, means you wont change the value of the **const **variable.

It is a **const-**ant.

> ##### \#include &lt;iostream&gt;
>
> ##### int main\(\)
>
> ##### {
>
> #####     const auto x = 100;
>
> #####     x = 200;     //Does not compile
>
> #####     //code stuffs
>
> #####     return \(0\);
>
> ##### }

**const** variables cannot be modified. This includes **const** pointers.

**const int \* **- a pointer that points to constant data.

**int\* const** - a pointer that cannot be reassigned.

**const int\* const** - a pointer that is constant, that points to data that is constant.

> const int a = 0xDEADBEEF;
>
> const int b = 0xCAFEF00D;
>
> int\* const ptr1 = &a;    //ERROR
>
> const int\* ptr2 = &a;
>
> ptr2 = &b;
>
> const int\* const ptr3 = &a;
>
> ptr3 = &b    //ERROR




# New to C++

##### **We now have the keyword: 'auto'**

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
>      auto x = 42.0L;
>
>      //code stuffs
>
>      return \(0\);
>
> }




# Namespaces

---

* Recall the topic of scope and local variables from C
* As C++ libraries begin to grow, name collisions could occur as your program could include multiple entities that define the same name.
* keyword namespace gives a new level of scope, so entities can be defined to a scope.
* **::** is the scope resolution operator, so you can reference an variable or function in a particular scope.
* keyword using allows your program to use an entire namespace.



> #### //bas.h
>
> #### namespace IQTCPP {
>
> ####      int foo;
>
> ####      class bar;
>
> ####      void bas\(\);
>
> #### }

> ### //some\_other\_file.cpp
>
> ### using namespace IQTCPP;
>
> ### using namespace IQTCPP::bas;
>
> ### 
>
> ### voiddo\_stuff\(\) {
>
> ###      foo = 10;
>
> ###      bar x;
>
> ###      IQTCPP::bas\(\);
>
> ### }
>
> ### …




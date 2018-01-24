# STL Linked Lists

---

* **std::list** – an STL doubly-linked list.

* Data is not contiguous.

* Random-access is slow, but insertion and removal is fast.

* You cannot use direct access with the** \[\] **operator or **.at\(\)**.

* There also exists **std::forward\_list** for a single linked list, if saving memory is a concern.

* You can still use all of the push/pop and emplace modifiers.

> ##### std::list&lt;char&gt; abc = {‘a’, ’b’, ’c’, …, ’x’, ‘y’, ‘z’};
>
> ##### 
>
> ##### for\(const auto& elem:abc\)
>
> ##### std::cout &lt;&lt; elem &lt;&lt; “ “;
>
> ##### std::cout &lt;&lt; “\n”;

---




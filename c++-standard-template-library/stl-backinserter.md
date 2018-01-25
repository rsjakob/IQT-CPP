# STL back\_inserter

---

A special kind of _iterator_, it allows algorithms to insert new elements to the end of a container \(and resizes the container\).

Can be used in containers that implement the **push\_back\(\) **method. These containers include **vector**, **deque**, and **list**.

There also exist **front\_inserters** and **regular inserters**, which use the **push\_front\(\)** and **insert\(\)** methods respectively.

> ##### vector&lt;int&gt; source{1, 2, 3, 4}, destination;
>
> ##### copy\(source.begin\(\), source.end\(\), back\_inserter\(destination\)\);
>
> ##### 
>
> ##### REQUIRE\(destination == vector&lt;int&gt;\({ 1, 2, 3, 4}\)\);

> ##### //Is this safer?

---


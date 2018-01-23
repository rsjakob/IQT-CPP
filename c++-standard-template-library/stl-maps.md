# STL Maps

---

* The **STL map ** is an associative container \(i.e. a key-value storage container\). IE they are referenced by their key and not their position in the container.
* No two elements can have the same key.

> ##### map&lt;string, string&gt; gundam;
>
> ##### bool found\_gundam = false;
>
> ##### gundam.emplace\(“AmuroRay”, “Gundam”\);
>
> ##### gundam.emplace\(“HeeroYuy”, “Wing Zero”\);
>
> ##### for\(const auto& element:found\_gundam\)
>
> ##### {
>
> ##### if\(element.first == “AmuroRay” && element.second == “Gundam”\)
>
> ##### {
>
> ##### found\_gundam= true;
>
> ##### }
>
> ##### }
>
> ##### 
>
> ##### REQUIRE\(found\_gundam\);

---

#### emplace\(\)

* **emplace\(const iterator position, Args && … args\)**
* Inserts an element into the **map**. Similar to **vectors, emplace\(\)**
* Constructs the new element in-place for lower overhead
* New to C++ 11

> gundam.emplace\(“Setsuna F. Seiei”, “Gundam Exia”\);

---

#### operator\[\]




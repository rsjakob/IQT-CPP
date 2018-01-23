
---

# STL Vector

---

**Vector **is a resizable array, with built-in methods and greater functionality than a C-String

* It helps to think of them as generic arrays.

Vector allocates an initial capacity, which can be set with **.reserve\(\) **and viewed with **.capacity\(\).**

* Memory is still stored contiguously.

There also exists **std::array**, which is a fixed size, and size must be known at compile time.

> ##### vector&lt;int&gt; primes{1, 2, 3, 5, 7, 11}
>
> ##### primes.emplace\_back\(13\);
>
> ##### int sum\_of\_primes= 0;
>
> ##### for\(const auto& element : primes\) {
>
> ##### sum\_of\_primes += element;
>
> ##### 
>
> ##### REQUIRE\(sum\_of\_primes == 42\);

---

#### operator\[\]

* You can still access elements of an array as you would a c-string, with the **operator\[\].**
* **Operator\[\] ** is unbounded, and a provided index-out-of-bounds will result in undefined behavior.
* **at\(\) ** provides a bounds-checked version.
* Keep in mind, you cant assign to a **const vector** element.

> ##### vector&lt;int&gt; fibonacci{0, 1, 1, 2, 3, 5, 8};
>
> ##### fibonacci\[0\] = 0;
>
> ##### fibonacci.at\(0\) = 0;
>
> ##### REQUIRE\(fibonacci\[3\] == 2\);
>
> ##### REQUIRE\(fibonacci.at\(3\) == 2\)

---

#### front\(\)

* Retrieves the first element in a container.
* Returns a reference, so you can assign it \(as long as its not **const**\).
* Behavior is undefined if the **vector **is empty.

> ##### vector&lt;int&gt; fibonacci{0, 1, 1, 2, 3, 5, 8};
>
> ##### fibonacci.front\(\) = 42;
>
> ##### REQUIRE\(fibonacci\[3\] == 42\);

---

#### back\(\)

* Returns the last element in a container.
* Returns a reference, so you can assign it \(as long as its not **const**\).
* Behavior is undefined if the **vector **is empty.

> ##### vector&lt;int&gt; fibonacci{0, 1, 1, 2, 3, 5, 8} ;
>
> ##### fibonacci.back\(\) = 42;
>
> ##### REQUIRE\(fibonacci.back\(\) == 42\);

---

#### data\(\)

* Returns a contiguous array of elements contained in the **vector.**
* You should only need this when interacting with C functions.
* New to C++11.

> ##### void do\_stuff\(constint\*x,intsize\_of\_x\);
>
> ##### vector&lt;int&gt; fibonaci\(0, 1, 1, 2, 3, 5, 8};
>
> ##### do\_stuff\(fibonacci.data\(\), fibonacci.size\(\)\);

---

#### emplace\_back\(\)

* **emplace\_back\(Args &&  … args\)**
* Adds an element to the end of the vector.
* The new element is constructed in place at the end of the vector using the provided argument.
* New to C++ 11.

> ##### vector&lt;int&gt; fibonacci{0, 1, 1, 2, 3, 5, 8} ;
>
> ##### fibonacci.emplace\_back\(42\)
>
> ##### REQUIRE\(fibonacci.size\(\) == 7\);
>
> ##### REQUIRE\(fibonacci.back\(\) == 42\);

---

#### empty\(\) and clear\(\)

**empty\(\)** – returns true if the vector contains no elements.

**clear\(\)** – removes all elements. Note that the removed elements are destroyed.

> ##### vector&lt;int&gt; fibonacci;
>
> ##### REQUIRE\(fibonacci.empty\(\)\);

##### 

> ##### vector&lt;int&gt; fibonacci{0, 1, 1, 2, 3, 5, 8};
>
> ##### fibonacci.clear\(\);
>
> ##### REQUIRE\(fibonacci.empty\(\)\);

---




# STL Deque

---

* Pronounced “deck”, short for “double-ended-queue”.
* Not guaranteed to be contiguous in memory.

> ##### std::deque&lt;int&gt; queue;
>
> ##### for\(auto i = 0U; i &lt; 10; ++i\)
>
> ##### queue.push\_front\(i\*i\);
>
> ##### while\(queue.size\(\) &gt; 0\)
>
> ##### {
>
> ##### std::cout &lt;&lt; queue.back\(\) &lt;&lt; “\n”;
>
> ##### queue.pop\_back\(\);
>
> ##### }

---

#### front\(\), push\_front\(\), and pop\_front\(\)

**.front\(\)** – retrieves an element from the front of the list.

**.push\_front\(\)** - Pushes an element to the front of the list.

**.pop\_front\(\)** – pops an element from the front of the list and deletes it.

> ##### std::deque&lt;int&gt; queue;
>
> ##### for\(auto i= 0U; i &lt; 10; ++i\)
>
> ##### queue.push\_front\(i\*i\);
>
> #####

##### 

> ##### for\(auto i= 0U; i &lt; 10; ++i\)
>
> ##### {
>
> ##### cout &lt;&lt; queue.front\(\) &lt;&lt; “\t”;
>
> ##### queue.pop\_front\(\);
>
> ##### }

---




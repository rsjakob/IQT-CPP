# STL Deque

---

* Pronounced “deck”, short for “double-ended-queue”.
* Not guaranteed to be contiguous in memory.

> std::deque&lt;int&gt; queue;
>
> for\(auto i = 0U; i &lt; 10; ++i\)
>
> queue.push\_front\(i\*i\);
>
>
>
> while\(queue.size\(\) &gt; 0\)
>
> {
>
> std::cout &lt;&lt; queue.back\(\) &lt;&lt; “\n”;
>
> queue.pop\_back\(\);
>
> }




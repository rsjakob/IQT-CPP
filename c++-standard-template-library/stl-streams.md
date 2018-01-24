# STL Streams

---

Streams provide a clean, serial interface for input and output \(I/O\) to arbitrary objects:

* devices
* console
* files
* C++ objects

Stream objects provide a layer of abstraction.

These stream operators are NOT the same as bitwise operators.

Stream objects are always to the left of the operator.

> ##### string soda;
>
> ##### cout &lt;&lt; “What kind of soda do want?” &lt;&lt; endl;
>
> ##### cin &gt;&gt; soda;
>
> ##### if\(soda == “Pepsi” \|\| soda == “pepsi”\)
>
> ##### {
>
> ##### cout &lt;&lt; “Coke it is” &lt;&lt; endl;
>
> ##### }

---

#### File Input

Files can be written to using streams.

Create the** ifstream **with the filename.

Check that the file was opened with **is\_open\(\)**.

Stream data into the **ifstream.**

Optional: clean up with **close\(\).**

> ##### ifstream file\(“streetfighter.txt”\);
>
> ##### if\(file.is\_open\(\)\) 
>
> ##### {
>
> ##### file &gt;&gt; “Hadoken!”;
>
> ##### file.close\(\);
>
> ##### } 
>
> ##### else 
>
> ##### {
>
> ##### cout&lt;&lt; “Unable to open file…”;
>
> ##### }

---


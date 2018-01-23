# Strings in C++

---

Stop using C-Strings

Instead use the std::string class

It is safer, more convenient, easier to use for common tasks, and memory usage is managed for you.

> ##### string fullname\(“Jeremy”\);
>
> ##### fullname += “Cantu”;
>
> ##### auto name\_length = fullname.length\(\);
>
> ##### auto space\_pos = fullname.length\(\);
>
> ##### auto last\_name = fullname.substr\(space\_pos + 1\);

We will discuss some import string class methods, but there are many, many more…some unique to C++ 11

There also exist other variants, such as std::wstring

---

#### length\(\):

returns the length of a string in bytes.

> ##### string keepcalm\(“Keep calm and carry on”\);
>
> ##### auto string\_len = keepcalm.length\(\);
>
> ##### REQUIRE\(string\_len== 21\);

---

#### substr\(\):

* **substr\(size\_t pos, size\_t len = npos\)** – returns a newly constructed substring of the original string.
* **string::npos** indicates all characters until the end of the string. This is a new feature to C++14
* **size\_t **is an unsigned int type.

> string keepcalm\(“Keep calm and kill zombies!”\);
>
> auto substring = keepcalm.substr\(14, 12\);
>
> REQUIRE\(substring == “kill zombies!”\);

---

#### find

**find\(const string& str\)** – returns the position of the first match. If no match is found, **string::npos** is returned.

> ##### string keepcalm\(“Keep calm and kill zombies!”\);
>
> ##### auto zpos = keepcalm.find\(“z”\);
>
> ##### REQUIRE\(zpos= 19\);

###### Note: other overloads of this method exist.

---

#### append

**append\(const string& str\)** - adds the given characters to the end of a string.

> ##### string keepcalm\(“Keep calm”\);
>
> ##### keepcalm.append\(“!”\);
>
> ##### REQUIRE\(keepcalm == “Keep calm!”\);

###### Note: other overloads of this method exist.

---

#### operator\[\]

* You can retrieve elements of a string with brackets \(like old C style array\[x\]\).
* If the index is out of bounds, you will get undefined behavior.
* Use at\(size\_t pos\) for a bounds-checked version.

> ##### string keepcalm\(“Keep calm and kill zombies!”\);
>
> ##### auto substring = keepcalm.substr\(14, 12\);
>
> ##### REQUIRE\(substring == “kill zombies!”\);

---

#### data and c\_str

* We can still use **string **objects in places where we still need C strings.
* We can retrieve the underlying C-string with **data\(\)** and** c\_str\(\)**.
* **c\_str\(\)** will return a null terminated string, **data\(\)** will not.

> ##### char old\_c\_function\(constchar\* x, int x\_len\);
>
> ##### string keepcalm\(“Keep calm”\);
>
> ##### auto result = old\_c\_function\(keepcalm.c\_str\(\), keepcalm.len\(\)\);

---




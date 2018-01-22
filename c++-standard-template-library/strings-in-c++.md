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
>
> ---




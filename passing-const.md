# Passing const

---

You can pass by reference/pointer/value with or without the **'const'** qualifier:

> double distance\_def\(const Point &point\){
>
> ```
>  return sqrt\(point.x \* point.x + point.y \* point.y\);
> ```
>
> };
>
> …

What's wrong with the following function declaration?

> double calculate\_stuff\(const Point point\);

---

# Passing by value

---

You can pass structs \(and classes\) by value:

> double distance\(Point point\){
>
> point.x \*= point.x;
>
> point.y \*= point.y;
>
> return sqrt\(point.x + point.y\);
>
> };
>
> …

---


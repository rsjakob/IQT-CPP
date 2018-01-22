# References

---

References are pointers that cannot be null, and you interact with references without having to use the dereference operator.

> struct Point{
>
> int x, y;
>
> };
>
>
>
> voidset\_to\_origin\(Point &point\){
>
>
>
> point.x = 0;
>
> point.y = 0;
>
> }
>
> …





> struct Point{
>
> int x, y;
>
> };
>
>
>
> void set\_to\_origin\(Point \*point\){
>
>
>
>  point-&gt;x = 0;
>
>  point-&gt;y = 0;
>
> }
>
> …




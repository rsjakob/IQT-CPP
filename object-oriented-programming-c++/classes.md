# Classes

---

Classes are user-defined types \(similar to structs\).

Consists of a set of data members \(variables, constants and functions\).

Classes can have some important functions for the purposes:

* Object initialization
* Copy
* Move
* Object destruction

Members are accessed with the **. **operator for objects, and **-&gt; **for pointers.

Operators like +, !, and \[\] can be defined for a class.

Classes are defined by the keyword **class**, which is like a _namespace _for its members.

> ##### class CyberBullet{
>
> #####  double velocity, position;
>
> ##### double time\_to\_target\_at\(doubletarget\_position\) 
>
> ##### {
>
> #####  return \(target\_position – position\) / velocity;
>
> #####  }
>
> ##### };

---

#### Class vs Struct

* Class members are private by default.
* Struct members are public by default.
* Syntactically they are very similar.

> class CyberBullet{
>
>  double velocity, position;
>
> double time\_to\_target\_at\(double target\_position\) 
>
> {
>
>  return \(target\_position – position\) / velocity;
>
>  }
>
> };
>
>
>
> struct CyberBullet{
>
>  double velocity, position;
>
>  double time\_to\_target\_at\(double target\_position\)
>
> {
>
>  return \(target\_position – position\) / velocity;
>
>  }
>
> };




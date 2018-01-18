# Headers and Source

**All of your knowledge from C translated to C++:**

* Put exported functionality in header \(.h\) files
* _\#include_ imported functionality from other headers
* Put implementation details in source fiels \(**.cpp**, not **.c**\)
* Do not use the **\#using** directive in a header

---

```
struct CyberMissile { 
  double velocity, position; 
  double time_to_target_at(double target_position){
    return (target_position – position)/velocity;
  }
};
```

###### You can opt to put the entire function definition in a header file.

----------------------------------------------------

```
cybermissile.h 

struct CyberMissile {
  double velocity, position;
double time_to_target_at(double target_position);
};

cybermissile.cpp

double CyberMissile::time_to_target_at(double target_position){
  return (target_position – position) / velocity;
}


```

###### Or we can split the declaration and definition into header and source files.




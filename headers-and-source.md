# Headers and Source

**All of your knowledge from C translated to C++:**

* Put exported functionality in header \(.h\) files
* _\#include_ imported functionality from other headers
* Put implementation details in source fiels \(**.cpp**, not **.c**\)
* Do not use the **\#using** directive in a header

----------------------------------

```
struct CyberMissile { 
  double velocity, position; 
  double time_to_target_at(double target_position){
    return (target_position – position)/velocity;
  }
};

```




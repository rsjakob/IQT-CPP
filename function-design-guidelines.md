# Function Design Guidelines

---

* Pass by **const **reference when you want to pass in an argument that will not be modified.
* Pass by value when you want a copy that you can modify.
* Never use raw pointers \(unless we are working with C functions\).

###### Note: consider whether you must operate on **const **arguments e.g. from an external API




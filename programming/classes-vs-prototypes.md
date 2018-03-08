The line between the two gets blurry once you look at the details of languages on both sides,
but the basic idea is that in prototypes, you don’t need to have some “class”-like construct
that represents a “kind of thing”. Methods can exist right on an individual object and objects
can inherit from(“delegate to” in prototypal lingo) each other.

With classes, state is on the instance, but for methods, there is always a level of **indirection**.
When you call a method, you look up the object’s class and then you find the method there.

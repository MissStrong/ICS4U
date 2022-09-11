## TODO

The **scope** of a variable refers to where and when variable can be used.

An **instance variable** is a variable that is declared within a class scope and it may be used anywhere within the object (and outside the object if it has the modifier `public`). It does not have the modifier `static`. Each object may have a different value for this variable.

A **class variable** is a variable that is declared within a class scope and has a shared value among all objects of the class. It has the modifier `static`. 

A **local variable** is a variable that is declared within a local scope. It may be used only within the context (e.g. a method or a loop) it was declared in. It is lost when its context is completed.

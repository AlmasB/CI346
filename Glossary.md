## CI346 Glossary (maintained by UoB students)

1. [Programming languages](#programming-languages)
2. [Concurrency](#concurrency)
3. [Client-server computing](#client-server-computing)

Programming Languages
---

**Object-oriented Paradigm**

Object-oriented (OO) programming solves computing concepts and problems by modelling objects. Objects have **states** and **behaviours**; for example, a person has a certain hair colour (state) and this person can change the colour(behaviour). **Inheritance** is part of the core functionality of objects in OO languages. **Classes** can have subclasses, which enables the subclass to inherit the methods and fields of its superclass. The core concept of inheritance is simple, but it can be used to model complex systems. **Encapsulation** is used to enclose methods and state in bundles and to restrict access to them.

Using _Java_ as the example language
```java
class Person {
    String hairColour;

    Person(String hairColour) {
        this.hairColour = hairColour;
    }

    void changeHairColour(final String colour){
        this.hairColour = colour;
    }
}

class Java {
    public static void main(String[] args) {
        Person pete = new Person("blue");

        System.out.println(pete.hairColour);
        pete.changeHairColour("white");
        System.out.println(pete.hairColour);
    }
}
```

-TODO: expand on this

**Functional Paradigm**  
Functional programming solves computing problems by chaining functions together. Functions are computations that have the same effect whether done once or multiple times (**idempotent**), similar to mathematical functions. They have referential transparency - that is a function always returns the same output for a given input. Typically there is no state and therefore no side-effects. Iterative loops are not allowed in functional programs, instead recursive calls are used.

Using _Haskell_ as the example language
```haskell
fib :: Integer -> Integer
fib 0 = 0
fib 1 = 1
fib n = fib (n-1) + fib (n-2)

main :: IO()
main = print (fib 10)
```
-TODO: expand on this



**Functional Paradigm vs Object-Oriented**

**SOLID Principles**

**Design Patterns**


Concurrency
---

**Process** - TODO


**Thread** - A thread is a spawnable unit of work in a program.
The Java Virtual Machine allows an application to have multiple threads of execution running concurrently.

[Source](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/lang/Thread.html)

```
Thread t = new Thread(() -> {
    // some code to run on new thread
});
t.start();
```

**Concurrency Advantages**

**Concurrency Issues and Solutions**


Client-server Computing
---

**TCP** - TODO

**UDP** - TODO

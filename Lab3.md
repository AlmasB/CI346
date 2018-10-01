### CI346 Lab Session 3

1. Imagine you have the following types:

```
public enum CourseType {
    CS, CSG, SE
}

public class Student {

    private String firstName;
    private String lastName;
    private int age;
    private CourseType courseType;
    
    // constructor
    // accessor methods (get / set)
}
```

Given a list of all students, `List<Student> students`,
implement a solution to the following problem using the OO approach:

Construct a `Map<CourseType, List<Student>>` that groups students into lists
by courses such that each student is aged 18 or over and their first name
is between "K" and "Z".

2. Implement a solution to the problem in (1) using the functional approach.

3. What is the difference between (1) and (2) in the way you think about the problem?

4. Consider the interface `Function`, see [link](https://docs.oracle.com/javase/8/docs/api/java/util/function/Function.html).
Create an object of type `Function` and assign a lambda expression to it.
For example:

```
Function<String, Integer> f = ...;
```

This is a function that takes a `String` and produces an `Integer`.
After you have assigned your lambda expression, use the object `f` on a `String`:

```
f.apply("Hello world");
```

This demonstrates the ability to represent functions / methods as objects.
Thus, you can pass `f` as an argument into another function.
This is how Java can do higher-order functions.
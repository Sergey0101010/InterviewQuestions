[Вопросы для собеседования](README.md)

# Java 8 to Java 21

## What's new in Java 21 и JDK 21?

- [Module system](https://openjdk.org/jeps/261) - Modules system, java 9
- [Local-Variable Type Inference](https://openjdk.org/jeps/286) -  java 10
- [Local-Variable Syntax for Lambda Parameters](https://openjdk.org/jeps/323) - java 11
- [Switch Expressions](https://openjdk.org/jeps/361) - New keyword `yield`, java 14 
- [Text blocks](https://openjdk.org/jeps/378) - java 15
- [Pattern Matching for instanceof](https://openjdk.org/jeps/394) - Java 16
- [Records](https://openjdk.org/jeps/395) - java 16
- [Sealed classes](https://openjdk.org/jeps/409) - java 17
- [Key Encapsulation Mechanism API](https://openjdk.org/jeps/452). Java 21
- [Generational ZGC](https://openjdk.org/jeps/439) - Improved performance Z Garbage Collector 
- [Record Patterns](https://openjdk.org/jeps/440) - Java 16
- [Virtual Threads](https://openjdk.org/jeps/444) - Release, java 21
- [Sequenced collections](https://openjdk.org/jeps/431) - java 21

## What is Java Platform Module System and what it's main purpose?
Java Platform Module System(JPMS) is new level of abstraction which was introduced in java 9, it is above packages.
Module is a group of closely related packages and resources along with a new module description file, you can
think of it as "package of packages".

Main motivation in creating modules in java was desire to add **strong encapsulation**, so by default a module
doesn't expose any of it's API to other modules. And now we need to explicitly open our API up to the world 
if we want it to be usable.

## What do you know about java type inference?
It's a new feature aimed to improve code readability, because as types grow in size it's getting harder to read 
code. 
It's basically allow you not to write type of local variables, replacing it with `var`, so you can replace 
`Stream<String> lines = Files.lines(path)` to `var lines = Files.lines(path)`

## What happens when the class you instantiate the class and assign to the variable declared with `var` which is implementing some interface?
Inferred type of the variable will be exactly _the class_, reference to the instance of which you're assigning the 
variable declared with `var`, other is impossible to realize, because what if our class implement multiple
interfaces, then how compiler should decide on which interface to infer for the variable

## Why you can't use `var` in the class level?
`var` was introduced with only purpose of improving the readability of code in java and **not**  to amend the 
Type System of the Java language, that's why you can't use it in the class level(for static or instance fields), 
because field might be used with polymorphism (might receive different implementation types, might be injected by IoC)
and at the byte code, it's not possible to dynamically change the field type for each different case

## Can you declare method parameter using `var`? 
`var` cannot be used for fields, method parameters, and method return types

## Is it allowed to assign `var` variable `null` value?
No, you'll get compile-time error. 

[Source](https://openjdk.org/projects/amber/guides/lvti-faq#Q7)

## Can you use `var` with diamond on the right-hand side?
Yes, you can. In this case you'll get your generic type replaced with `Object` 
`var list = new ArrayList<>(); `  ArrayList<Object>() 

## Is `var` variable final?
No, local variables declared with `var` are non-final by default. But you can declare them as final
`final var = new Person();` 

## Can you use `var` with lambda parameters?
Yes, you can do it. 
If lambda expression may be _implicitly typed_ like this: `(x, y) -> x.process(y)` in java 11 you can now do
`(var x, var y) -> x.process(y)` this thing is basically done for uniformity with local variables and 
using `var` in implicit lambdas you can apply to it's parameters annotations like `@Nonnull` 



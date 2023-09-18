[Вопросы для собеседования](README.md)

# Java 8 to Java 21

## What's new in Java 21 и JDK 21?

- [Module system](https://openjdk.org/jeps/261) - Modules system, java 9
- [Local-Variable Type Inference](https://openjdk.org/jeps/286) -  java 10
- [Local-Variable Syntax for Lambda Parameters](https://openjdk.org/jeps/323) - java 11
- [Switch Expressions](https://openjdk.org/jeps/361) - New keyword `yield` and `switch` expression java 14 
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
using `var` in implicit lambdas you can apply to its parameters annotations like `@Nonnull` 

## What is switch expression and what how it differs from switch statement?
In older versions of java than java 14, were only switch statements, which allow you to check some 
condition for multivalued variable, and in java 14 _switch expression_ was released. 
Like any expression, `switch` expression evaluate to a single value, and can be used in statements, it also 
introduced _arrow case_ labels eliminating need for `break` statements to prevent fall through.

Ex:
```java
enum PaymentStatus {
    UNPAID, PARTPAID, PAID, DISPUTED, UNKNOWN;
}

public class Main {
    public static void main(String[] args) {
        PaymentStatus paymentStatus = PaymentStatus.PARTPAID;

        String message = switch (paymentStatus) {
        case UNPAID -> "The order has not been paid yet. Please make the minimum/full amount to procced.";
        case PARTPAID -> "The order is partially paid. Some features will not be available. Please check the brochure for details.";
        case PAID -> "The order is fully paid. Please choose the desired items from the menu.";
        default -> throw new IllegalStateException("Invalid payment status: " + paymentStatus);
        };

        System.out.println(message);
    }
}
```

## What is the keyword `yield` used for?
Keyword `yield` is used in `switch` expression instead of the narrow operator to return a value from `switch` 
expression.
```java
public class Main {
    public static void main(String[] args) {
        PaymentStatus paymentStatus = PaymentStatus.PARTPAID;

        String message = switch (paymentStatus) {
        case UNPAID:
            yield "The order has not been paid yet. Please make the minimum/full amount to procced.";
        case PARTPAID:
            yield "The order is partially paid. Some features will not be available. Please check the brochure for details.";
        case PAID:
            yield "The order is fully paid. Please choose the desired items from the menu.";
        default:
            throw new IllegalStateException("Invalid payment status: " + paymentStatus);
        };

        System.out.println(message);
    }
}
```

## What is text block in java?
Text blocks are the java 15 feature allowed new more readable way of writing multiline strings, text block
starts with a """ followed by newline
```java
String example = """
    Example text""";
```
Result of a text block is still a string, text blocks just provide us with another way to write String literals 
in our source code. 

Inside the text blocks, we can freely use newlines and quotes without the need for escaping line breaks.

## Is it allowed to use _formatting_ with text blocks?
Yes, you can use `String.format()` method directly on text block
```java
public String getFormattedText(String parameter) {
    return """
            Some parameter: %s
            """.formatted(parameter);
}
```
## What is pattern matching for instanceof?
Pattern matching involves testing whether an object has a particular structure, then extracting data from that 
object if there's a match. You can already do this in java, but since release of java 16, you have new
language enhancements that enable you to conditionally extract data from object.

```java
public static double getPerimeter(Shape shape) throws IllegalArgumentException {
        if (shape instanceof Rectangle r) { // instead of casting after
            return 2 * r.length() + 2 * r.width();
        } else if (shape instanceof Circle c) {
            return 2 * c.radius() * Math.PI;
        } else {
            throw new IllegalArgumentException("Unrecognized shape");
        }
    }
```

## Tell about record classes
Record classes are a special kind of class, help to model plain aggregates with less boilerplate 
than normal classes.
A record declaration specifies in a header a description of its contents, the appropriate accessors, constructor, 
`equals()`, `hashCode()`, `toString` are created automatically. A record's fields are `final`. 

```java
record Rectangle(double length, double width) { }
```
Automatically generates getters for all fields, like `length()` and `width()`, both fields are `final`

## Is it possible to create custom getters or other by-default implemented methods in record?
Yes, it is possible to change any of the methods inside record class, just write same signature
as it was before
```java
record Rectangle(double length, double width) {
 
    public double length() {
        System.out.println("Length is " + length);
        return length;
    }
}
```

## What are you allowed to place inside record class?
1. You can declare canonic record constructor(All args constructor) 
```java
record Rectangle(double length, double width) {
    public Rectangle {
        if (length <= 0 || width <= 0) {
            throw new java.lang.IllegalArgumentException(
                String.format("Invalid dimensions: %f, %f", length, width));
        }
    }
}
```
2. public getter methods(just use same signature)
3. Declare static fields, static initializers, static methods, and they behave as they would in normal class
4. You can declare instance methods in a record class, nested classes, even nested record classes(static implicitly)

You can't declare non-static fields inside records, and you can't declare `native` methods inside records

## Are you allowed to create record which implements some interface or using generics?
Yes, you can in both cases
`record Customer(..) implements Billable{}`
 
`record Triangle<C extends Coordinate> (..)`

## what are sealed classes in java and why we need them
Sealing allows classes and interfaces to define their permitted subtypes.
With sealing, we increase clarity of code

## give an example of sealed interface
Permits section should be defined after any extends or implements clause

public sealed interface Service permits
Car, Truck {

}

## is it allowed to extend class which is in sealed hierarchy
Subclasses of sealed class or interfaces must explicitly define modifier:  final, sealed, non-sealed

If we define class as non sealed, then it might be super class of any other class

## what is key encapsulation API

Key encapsulation is a modern cryptographic technique 
that secures symmetric keys using asymmetric or public key cryptography

key encapsulation mechanism (KEM) instead uses properties of the public key to derive a related symmetric key, which requires no padding
Kem consists of three functions
⁃ Key pair generation function
⁃ Key encapsulation function, called by sender
⁃ Key decapsulation function

Key pair generation function already exist(KeyPairGenerator API), so kem API defines encapsulation and decapsulation functions

## what is record pattern?
A record pattern is a construct that allows us to match values against a record type and bind variables to corresponding components of the record

Example:
```java

if (o instanceof Location (String name, GPSPoint gpsPoint)) {
System.out.println(name);
}

if (o instanceof Location (var name, GPSPoint(var latitude, var longitude))) {
System.out.println("lat: " + latitude + ", lng: " + longitude);
}

We can access record variables if instance of evaluates to true, it is true only if o variable has exactly matching type with comparing type

We also can use record patterns in switch expression

Double result = switch (object) {
case Location(var name, GPSPoint(var latitude, var longitude)) -> latitude;
default -> 0.0;
};
```

## can we use record patterns with generics Like Record <Record 2>
Yes, we can
```java
Wrapper<Location> wrapper = new Wrapper<>(new Location("Home", new GPSPoint(1.0, 2.0)), "Description");
if (wrapper instanceof Wrapper<Location>(var location, var description)) {
System.out.println(description);
}
```

## What are sequenced collections and why they were added?
A sequenced collection is a Collection which elements have a defined encounter order. 
A sequenced collection has first and last elements and every element between them has successors and predecessors

## What methods do sequenced collections have

``` java
interface SequencedCollection<E> extends Collection<E> {
// new method
SequencedCollection<E> reversed();
// methods promoted from Deque
void addFirst(E);
void addLast(E);
E getFirst();
E getLast();
E removeFirst();
E removeLast();
}
```
## What subtypes of sequenced collections do you know
SequencedSet<T> for collections where you can't add duplicates
SequencedMap<T> for maps which support entries order


[Вопросы для собеседования](README.md)

# Java Core
+ [What are the differences between JRE, JVM and JDK?](#what-are-the-differences-between-jre-jvm-and-jdk)
+ [Is java interpreted or compiled language?](#is-java-interpreted-or-compiled-language)
+ [When does java interpret the bytecode and when does it compile it?](#when-does-java-interpret-the-bytecode-and-when-does-it-compile-it)
+ [What types of access modifiers are existing in java?](#what-types-of-access-modifiers-are-existing-in-java)
+ [О чем говорит ключевое слово `final`?](#О-чем-говорит-ключевое-слово-final)
+ [Какими значениями инициализируются переменные по умолчанию?](#Какими-значениями-инициализируются-переменные-по-умолчанию)
+ [Что вы знаете о функции `main()`?](#Что-вы-знаете-о-функции-main)
+ [Какие логические операции и операторы вы знаете?](#Какие-логические-операции-и-операторы-вы-знаете)
+ [Что такое тернарный оператор выбора?](#Что-такое-тернарный-оператор-выбора)
+ [Какие побитовые операции вы знаете?](#Какие-побитовые-операции-вы-знаете)
+ [Где и для чего используется модификатор `abstract`?](#Где-и-для-чего-используется-модификатор-abstract)
+ [Дайте определение понятию _«интерфейс»_. Какие модификаторы по умолчанию имеют поля и методы интерфейсов?](#Дайте-определение-понятию-интерфейс-Какие-модификаторы-по-умолчанию-имеют-поля-и-методы-интерфейсов)
+ [What is the difference between abstract class and interface? In which scenario it is more appropriate to use an abstract class rather than the interface(s)?](#what-is-the-difference-between-abstract-class-and-interface-in-which-scenario-it-is-more-appropriate-to-use-an-abstract-class-rather-than-the-interfaces)
+ [Почему в некоторых интерфейсах вообще не определяют методов?](#Почему-в-некоторых-интерфейсах-вообще-не-определяют-методов)
+ [Почему нельзя объявить метод интерфейса с модификатором `final`?](#Почему-нельзя-объявить-метод-интерфейса-с-модификатором-final)
+ [Что имеет более высокий уровень абстракции - _класс_, _абстрактный класс_ или _интерфейс_?](#Что-имеет-более-высокий-уровень-абстракции---класс-абстрактный-класс-или-интерфейс)
+ [Может ли объект получить доступ к члену класса, объявленному как `private`? Если да, то каким образом?](#Может-ли-объект-получить-доступ-к-члену-класса-объявленному-как-private-Если-да-то-каким-образом)
+ [Каков порядок вызова конструкторов и блоков инициализации с учётом иерархии классов?](#Каков-порядок-вызова-конструкторов-и-блоков-инициализации-с-учётом-иерархии-классов)
+ [Зачем нужны и какие бывают блоки инициализации?](#Зачем-нужны-и-какие-бывают-блоки-инициализации)
+ [К каким конструкциям Java применим модификатор `static`?](#К-каким-конструкциям-java-применим-модификатор-static)
+ [Для чего в Java используются статические блоки инициализации?](#Для-чего-в-java-используются-статические-блоки-инициализации)
+ [Что произойдёт, если в блоке инициализации возникнет исключительная ситуация?](#Что-произойдёт-если-в-блоке-инициализации-возникнет-исключительная-ситуация)
+ [Какое исключение выбрасывается при возникновении ошибки в блоке инициализации класса?](#Какое-исключение-выбрасывается-при-возникновении-ошибки-в-блоке-инициализации-класса)
+ [Может ли статический метод быть переопределён или перегружен?](#Может-ли-статический-метод-быть-переопределён-или-перегружен)
+ [Могут ли нестатические методы перегрузить статические?](#Могут-ли-нестатические-методы-перегрузить-статические)
+ [Is Java "pass-by-reference" or "pass-by-value"?](#is-java-pass-by-reference-or-pass-by-value)
+ [Можно ли сузить уровень доступа/тип возвращаемого значения при переопределении метода?](#Можно-ли-сузить-уровень-доступатип-возвращаемого-значения-при-переопределении-метода)
+ [Возможно ли при переопределении метода изменить: модификатор доступа, возвращаемый тип, тип аргумента или их количество, имена аргументов или их порядок; убирать, добавлять, изменять порядок следования элементов секции `throws`?](#Возможно-ли-при-переопределении-метода-изменить-модификатор-доступа-возвращаемый-тип-тип-аргумента-или-их-количество-имена-аргументов-или-их-порядок-убирать-добавлять-изменять-порядок-следования-элементов-секции-throws)
+ [Как получить доступ к переопределенным методам родительского класса?](#Как-получить-доступ-к-переопределенным-методам-родительского-класса)
+ [Можно ли объявить метод абстрактным и статическим одновременно?](#Можно-ли-объявить-метод-абстрактным-и-статическим-одновременно)
+ [В чем разница между членом экземпляра класса и статическим членом класса?](#В-чем-разница-между-членом-экземпляра-класса-и-статическим-членом-класса)
+ [Где разрешена инициализация статических/нестатических полей?](#Где-разрешена-инициализация-статическихнестатических-полей)
+ [Какие типы классов бывают в java?](#Какие-типы-классов-бывают-в-java)
+ [Расскажите про вложенные классы. В каких случаях они применяются?](#Расскажите-про-вложенные-классы-В-каких-случаях-они-применяются)
+ [Что такое _«статический класс»_?](#Что-такое-статический-класс)
+ [Какие существуют особенности использования вложенных классов: статических и внутренних? В чем заключается разница между ними?](#Какие-существуют-особенности-использования-вложенных-классов-статических-и-внутренних-В-чем-заключается-разница-между-ними)
+ [Что такое _«локальный класс»_? Каковы его особенности?](#Что-такое-локальный-класс-Каковы-его-особенности)
+ [Что такое _«анонимные классы»_? Где они применяются?](#Что-такое-анонимные-классы-Где-они-применяются)
+ [Каким образом из вложенного класса получить доступ к полю внешнего класса?](#Каким-образом-из-вложенного-класса-получить-доступ-к-полю-внешнего-класса)
+ [Для чего используется оператор `assert`?](#Для-чего-используется-оператор-assert)
+ [Что такое _Heap_ и _Stack_ память в Java? Какая разница между ними?](#Что-такое-heap-и-stack-память-в-java-Какая-разница-между-ними)
+ [Верно ли утверждение, что примитивные типы данных всегда хранятся в стеке, а экземпляры ссылочных типов данных в куче?](#Верно-ли-утверждение-что-примитивные-типы-данных-всегда-хранятся-в-стеке-а-экземпляры-ссылочных-типов-данных-в-куче)
+ [Каким образом передаются переменные в методы, по значению или по ссылке?](#Каким-образом-передаются-переменные-в-методы-по-значению-или-по-ссылке)
+ [Для чего нужен сборщик мусора?](#Для-чего-нужен-сборщик-мусора)
+ [Как работает сборщик мусора?](#Как-работает-сборщик-мусора)
+ [What types of Garbage collectors exist in HotSpot JVM?](#what-types-of-garbage-collectors-exist-in-hotspot-jvm)
+ [Опишите алгоритм работы какого-нибудь сборщика мусора, реализованного в виртуальной машине HotSpot.](#Опишите-алгоритм-работы-какого-нибудь-сборщика-мусора-реализованного-в-виртуальной-машине-hotspot)
+ [Что такое «пул строк»?](#Что-такое-пул-строк)
+ [Что такое `finalize()`? Зачем он нужен?](#Что-такое-finalize-Зачем-он-нужен)
+ [Что произойдет со сборщиком мусора, если выполнение метода `finalize()` требует ощутимо много времени, или в процессе выполнения будет выброшено исключение?](#Что-произойдет-со-сборщиком-мусора-если-выполнение-метода-finalize-требует-ощутимо-много-времени-или-в-процессе-выполнения-будет-выброшено-исключение)
+ [Чем отличаются `final`, `finally` и `finalize()`?](#Чем-отличаются-final-finally-и-finalize)
+ [Расскажите про приведение типов. Что такое понижение и повышение типа?](#Расскажите-про-приведение-типов-Что-такое-понижение-и-повышение-типа)
+ [Когда в приложении может быть выброшено исключение `ClassCastException`?](#Когда-в-приложении-может-быть-выброшено-исключение-classcastexception)
+ [Что такое литералы?](#Что-такое-литералы)
+ [Что такое _autoboxing («автоупаковка»)_ в Java и каковы правила упаковки примитивных типов в классы-обертки?](#Что-такое-autoboxing-автоупаковка-в-java-и-каковы-правила-упаковки-примитивных-типов-в-классы-обертки)
+ [Какие есть особенности класса `String`?](#Какие-есть-особенности-класса-string)
+ [Почему `String` неизменяемый и финализированный класс?](#Почему-string-неизменяемый-и-финализированный-класс)
+ [Почему `char[]` предпочтительнее `String` для хранения пароля?](#Почему-char-предпочтительнее-string-для-хранения-пароля)
+ [Почему строка является популярным ключом в `HashMap` в Java?](#Почему-строка-является-популярным-ключом-в-hashmap-в-java)
+ [Что делает метод `intern()` в классе `String`?.](#Что-делает-метод-intern-в-классе-string)
+ [Можно ли использовать строки в конструкции `switch`?](#Можно-ли-использовать-строки-в-конструкции-switch)
+ [Какая основная разница между `String`, `StringBuffer`, `StringBuilder`?](#Какая-основная-разница-между-string-stringbuffer-stringbuilder)
+ [Что такое класс `Object`? Какие в нем есть методы?](#Что-такое-класс-object-Какие-в-нем-есть-методы)
+ [Is an array an object in Java?](#is-an-array-an-object-in-java)
+ [Дайте определение понятию «конструктор».](#Дайте-определение-понятию-конструктор)
+ [Что такое _«конструктор по умолчанию»_?](#Что-такое-конструктор-по-умолчанию)
+ [Чем отличаются конструктор по-умолчанию, конструктор копирования и конструктор с параметрами?](#Чем-отличаются-конструктор-по-умолчанию-конструктор-копирования-и-конструктор-с-параметрами)
+ [Где и как вы можете использовать приватный конструктор?](#Где-и-как-вы-можете-использовать-приватный-конструктор)
+ [Расскажите про классы-загрузчики и про динамическую загрузку классов.](#Расскажите-про-классы-загрузчики-и-про-динамическую-загрузку-классов)
+ [Что такое _Reflection_?](#Что-такое-reflection)
+ [Why is `equals()` needed? How does it differ from the `==` operation](#why-is-equals-needed-how-does-it-differ-from-the--operation)
+ [Если вы хотите переопределить `equals()`, какие условия должны выполняться?](#Если-вы-хотите-переопределить-equals-какие-условия-должны-выполняться)
+ [Какими свойствами обладает порождаемое `equals()` отношение эквивалентности?](#Какими-свойствами-обладает-порождаемое-equals-отношение-эквивалентности)
+ [Правила переопределения метода `Object.equals()`.](#Правила-переопределения-метода-objectequals)
+ [Какая связь между `hashCode()` и `equals()`?](#Какая-связь-между-hashcode-и-equals)
+ [Если `equals()` переопределен, есть ли какие-либо другие методы, которые следует переопределить?](#Если-equals-переопределен-есть-ли-какие-либо-другие-методы-которые-следует-переопределить)
+ [Что будет, если переопределить `equals()` не переопределяя `hashCode()`? Какие могут возникнуть проблемы?](#Что-будет-если-переопределить-equals-не-переопределяя-hashcode-Какие-могут-возникнуть-проблемы)
+ [Каким образом реализованы методы `hashCode()` и `equals()` в классе `Object`?](#Каким-образом-реализованы-методы-hashcode-и-equals-в-классе-object)
+ [Для чего нужен метод `hashCode()`?](#Для-чего-нужен-метод-hashcode)
+ [Каковы правила переопределения метода `Object.hashCode()`?](#Каковы-правила-переопределения-метода-objecthashcode)
+ [Есть ли какие-либо рекомендации о том, какие поля следует использовать при подсчете `hashCode()`?](#Есть-ли-какие-либо-рекомендации-о-том-какие-поля-следует-использовать-при-подсчете-hashcode)
+ [Могут ли у разных объектов быть одинаковые `hashCode()`?](#Могут-ли-у-разных-объектов-быть-одинаковые-hashcode)
+ [Если у класса `Point{int x, y;}` реализовать метод `equals(Object that) {(return this.x == that.x && this.y == that.y)}`, но сделать хэш код в виде `int hashCode() {return x;}`, то будут ли корректно такие точки помещаться и извлекаться из `HashSet`?](#Если-у-класса-pointint-x-y-реализовать-метод-equalsobject-that-return-thisx--thatx--thisy--thaty-но-сделать-хэш-код-в-виде-int-hashcode-return-x-то-будут-ли-корректно-такие-точки-помещаться-и-извлекаться-из-hashset)
+ [Могут ли у разных объектов `(ref0 != ref1)` быть `ref0.equals(ref1) == true`?](#Могут-ли-у-разных-объектов-ref0--ref1-быть-ref0equalsref1--true)
+ [Могут ли у разных ссылок на один объект `(ref0 == ref1)` быть `ref0.equals(ref1) == false`?](#Могут-ли-у-разных-ссылок-на-один-объект-ref0--ref1-быть-ref0equalsref1--false)
+ [Можно ли так реализовать метод `equals(Object that) {return this.hashCode() == that.hashCode()}`?](#Можно-ли-так-реализовать-метод-equalsobject-that-return-thishashcode--thathashcode)
+ [В `equals()` требуется проверять, что аргумент `equals(Object that)` такого же типа что и сам объект. В чем разница между `this.getClass() == that.getClass()` и `that instanceof MyClass`?](#В-equals-требуется-проверять-что-аргумент-equalsobject-that-такого-же-типа-что-и-сам-объект-В-чем-разница-между-thisgetclass--thatgetclass-и-that-instanceof-myclass)
+ [Можно ли реализовать метод `equals()` класса `MyClass` вот так: `class MyClass {public boolean equals(MyClass that) {return this == that;}}`?](#Можно-ли-реализовать-метод-equals-класса-myclass-вот-так-class-myclass-public-boolean-equalsmyclass-that-return-this--that)
+ [Есть класс `Point{int x, y;}`. Почему хэш код в виде `31 * x + y` предпочтительнее чем `x + y`?](#Есть-класс-pointint-x-y-Почему-хэш-код-в-виде-31--x--y-предпочтительнее-чем-x--y)
+ [Расскажите про интерфейс `Comparable<T>`, чем он отличается от интерфейса `Comparator<T>`?](#расскажите-про-интерфейс-comparablet-чем-он-отличается-от-интерфейса-comparatort)
+ [Почему при реализации методов `compareTo()` и `compare()` интерфейсов `Comparable<T>` и `Comparator<T>` соответственно, необходимо их согласование с `equals()`?](#почему-при-реализации-методов-compareto-и-compare-интерфейсов-comparablet-и-comparatort-соответственно-необходимо-их-согласование-с-equals)
+ [Расскажите про клонирование объектов.](#Расскажите-про-клонирование-объектов)
+ [В чем отличие между _поверхностным_ и _глубоким_ клонированием?](#В-чем-отличие-между-поверхностным-и-глубоким-клонированием)
+ [Какой способ клонирования предпочтительней?](#Какой-способ-клонирования-предпочтительней)
+ [Почему метод `clone()` объявлен в классе `Object`, а не в интерфейсе `Cloneable`?](#Почему-метод-clone-объявлен-в-классе-object-а-не-в-интерфейсе-cloneable)
+ [Опишите иерархию исключений.](#Опишите-иерархию-исключений)
+ [Какие виды исключений в Java вы знаете, чем они отличаются?](#Какие-виды-исключений-в-java-вы-знаете-чем-они-отличаются)
+ [Что такое _checked_ и _unchecked exception_?](#Что-такое-checked-и-unchecked-exception)
+ [Какой оператор позволяет принудительно выбросить исключение?](#Какой-оператор-позволяет-принудительно-выбросить-исключение)
+ [О чем говорит ключевое слово `throws`?](#О-чем-говорит-ключевое-слово-throws)
+ [Как написать собственное («пользовательское») исключение?](#Как-написать-собственное-пользовательское-исключение)
+ [Какие существуют _unchecked exception_?](#Какие-существуют-unchecked-exception)
+ [Что представляет из себя ошибки класса `Error`?](#Что-представляет-из-себя-ошибки-класса-error)
+ [Что вы знаете о `OutOfMemoryError`?](#Что-вы-знаете-о-outofmemoryerror)
+ [Опишите работу блока _try-catch-finally_.](#Опишите-работу-блока-try-catch-finally)
+ [Что такое механизм _try-with-resources_?](#Что-такое-механизм-try-with-resources)
+ [Возможно ли использование блока _try-finally_ (без `catch`)?](#Возможно-ли-использование-блока-try-finally-без-catch)
+ [Может ли один блок `catch` отлавливать сразу несколько исключений?](#Может-ли-один-блок-catch-отлавливать-сразу-несколько-исключений)
+ [Всегда ли исполняется блок `finally`?](#Всегда-ли-исполняется-блок-finally)
+ [Существуют ли ситуации, когда блок `finally` не будет выполнен?](#Существуют-ли-ситуации-когда-блок-finally-не-будет-выполнен)
+ [Может ли метод _main()_ выбросить исключение во вне и если да, то где будет происходить обработка данного исключения?](#Может-ли-метод-main-выбросить-исключение-во-вне-и-если-да-то-где-будет-происходить-обработка-данного-исключения)
+ [Предположим, есть метод, который может выбросить `IOException` и `FileNotFoundException` в какой последовательности должны идти блоки `catch`? Сколько блоков `catch` будет выполнено?](#Предположим-есть-метод-который-может-выбросить-ioexception-и-filenotfoundexception-в-какой-последовательности-должны-идти-блоки-catch-Сколько-блоков-catch-будет-выполнено)
+ [Что такое _generics_?](#Что-такое-generics)
+ [Что такое _«интернационализация»_, _«локализация»_?](#Что-такое-интернационализация-локализация)

## What are the differences between JRE, JVM and JDK?
__JVM__, Java Virtual Machine — main part of JRE. JVM is responsible for converting the byte code to the machine specific code. JVM is also platform dependendent
and differs on windows, mac, linux and other Operating Systems.

__JRE__, Java Runtime Environment - set of necessary software tools which are used to run Java program. Consists of JVM and java standard library.

__JDK__, Java Development Kit - JRE and set of developer tools Java, including Java compiler, code examples, documentation and some other tools.

Briefly: __JDK__ - development environment for Java programs, including __JRE__ - environment for running Java programs,
which in its turn contains __JVM__ - code interpreter.

[to the top](#java-core)

## What you need to install on your server or computer to only run some java program which is stored as .jar file?
In this case JRE will be enough.

## Is java interpreted or compiled language?
Java implementations typically use a two-step compilation process.
Code written in Java is:
First compiled to bytecode by a program called `javac`

Then, another program called `java` starts the Java runtime environment and 
it may **compile and/or interpret** the bytecode by using 
the Java Interpreter/JIT Compiler. 

But it's true only for HotSpot JVM, other JVM's may use other technics like 
Ahead-of-time(AOT) compilation

[to the top](#java-core)

## When does java interpret the bytecode and when does it compile it?

The application code is initially interpreted, but the JVM monitors which sequences 
of bytecode are frequently executed and translates them to machine code for direct 
execution on the hardware. For bytecode which is executed only a few times, this 
saves the compilation time and reduces the initial latency; 
for frequently executed bytecode, JIT compilation is used to run at high speed,
after an initial phase of slow interpretation. 
Additionally, since a program spends most time executing a minority of its code,
the reduced compilation time is significant. 
Finally, during the initial code interpretation, execution statistics can be 
collected before compilation, which helps to perform better optimization

[Stackoverflow](https://stackoverflow.com/a/36394113)
[to the top](#java-core)

## What types of access modifiers are existing in java?
__private__: The access level of a private modifier is only within the class. It cannot be accessed from outside the class. Denoted by keyword `private`.

__default__, package-private, package level The access level of a default modifier is only within the package. It cannot be accessed from outside the package.
If you do not specify any access level, it will be the default

__protected__  The access level of a protected modifier is within the package and outside the package through child class.
If you do not make the child class, it cannot be accessed from outside the package. Denoted by keyword `protected`.

__public__ The access level of a public modifier is everywhere. It can be accessed from within the class,
outside the class, within the package and outside the package. Denoted by keyword `public`.

Access modifiers from less restrictive to most restrictive: public, protected, default, private.

It is possible to make the access less restrictive, for example from `protected` to `public`.

[to the top](#java-core)

## О чем говорит ключевое слово `final`?
Модификатор `final` может применяться к переменным, параметрам методов, полям и методам класса или самим классам.

+ Класс не может иметь наследников;
+ Метод не может быть переопределен в классах наследниках;
+ Поле не может изменить свое значение после инициализации;
+ Параметры методов не могут изменять своё значение внутри метода;
+ Локальные переменные не могут быть изменены после присвоения им значения.

[to the top](#java-core)

## How to create immutable class?
To make your class immutable you should:
1. Declare class as `final`so it can't be extended
2. Make all the fields `private` 
3. Make all fields `final` so they can't been changed later
4. Init all fields through constructor and all mutable fields should be created through deep copy
5. For all getters which return mutable fields you should return their deep copy

```java
public final class FinalClassExample {
  private final int id;

  private final String name;

  private final HashMap<String,String> testMap;


  public int getId() {
    return id;
  }

  public String getName() {
    return name;
  }

  // Getter function for mutable objects

  public HashMap<String, String> getTestMap() {
    return (HashMap<String, String>) testMap.clone();
  }

  // Constructor method performing deep copy

  public FinalClassExample(int i, String n, HashMap<String,String> hm){
    System.out.println("Performing Deep Copy for Object initialization");

    // "this" keyword refers to the current object
    this.id=i;
    this.name=n;

    HashMap<String,String> tempMap=new HashMap<String,String>();
    String key;
    Iterator<String> it = hm.keySet().iterator();
    while(it.hasNext()){
      key=it.next();
      tempMap.put(key, hm.get(key));
    }
    this.testMap=tempMap;
  
}
```


## Какими значениями инициализируются переменные по умолчанию?
+ Числа инициализируются `0` или `0.0`; 
+ `char` — `\u0000`;
+ `boolean` — `false`;
+ Объекты (в том числе `String`) — `null`.

[to the top](#java-core)

## Что вы знаете о функции `main()`?

Метод `main()` — точка входа в программу. В приложении может быть несколько таких методов. Если метод отсутствует, то компиляция возможна, но при запуске будет получена ошибка _\`Error: Main method not found\`_.

```java 
public static void main(String[] args) {}
```

[to the top](#java-core)

## Какие логические операции и операторы вы знаете?
+ `&`: Логическое _AND_ (И);
+ `&&`: Сокращённое _AND_;
+ `|`: Логическое _OR_ (ИЛИ);
+ `||`: Сокращённое _OR_;
+ `^`: Логическое _XOR_ (исключающее _OR_ (ИЛИ));
+ `!`: Логическое унарное _NOT_ (НЕ);
+ `&=`: _AND_ с присваиванием;
+ `|=`: _OR_ с присваиванием;
+ `^=`: _XOR_ с присваиванием;
+ `==`: Равно;
+ `!=`: Не равно;
+ `?:`: Тернарный (троичный) условный оператор.

[to the top](#java-core)

## Что такое тернарный оператор выбора?
Тернарный условный оператор `?:` - оператор, которым можно заменить некоторые конструкции операторов `if-then-else`.

Выражение записывается в следующей форме:
>условие ? выражение1 : выражение2

Если `условие` выполняется, то вычисляется `выражение1` и его результат становится результатом выполнения всего оператора. Если же `условие` равно `false`, то вычисляется `выражение2` и его значение становится результатом работы оператора. Оба операнда `выражение1` и `выражение2` должны возвращать значение одинакового (или совместимого) типа.

[to the top](#java-core)

## Какие побитовые операции вы знаете?
+ `~`: Побитовый унарный оператор NOT;
+ `&`: Побитовый AND;
+ `&=`: Побитовый AND с присваиванием;
+ `|`: Побитовый OR;
+ `|=`: Побитовый OR с присваиванием;
+ `^`: Побитовый исключающее XOR;
+ `^=`: Побитовый исключающее XOR с присваиванием;
+ `>>`: Сдвиг вправо (деление на 2 в степени сдвига);
+ `>>=`: Сдвиг вправо с присваиванием;
+ `>>>`: Сдвиг вправо без учёта знака;
+ `>>>=`: Сдвиг вправо без учёта знака с присваиванием;
+ `<<`: Сдвиг влево (умножение на 2 в степени сдвига);
+ `<<=`: Сдвиг влево с присваиванием.

[to the top](#java-core)

## Где и для чего используется модификатор `abstract`?
Класс, помеченный модификатором `abstract`, называется абстрактным классом. Такие классы могут выступать только предками для других классов. Создавать экземпляры самого абстрактного класса не разрешается. При этом наследниками абстрактного класса могут быть как другие абстрактные классы, так и классы, допускающие создание объектов.

Метод, помеченный ключевым словом `abstract` - абстрактный метод, т.е. метод, который не имеет реализации. Если в классе присутствует хотя бы один абстрактный метод, то весь класс должен быть объявлен абстрактным.

Использование абстрактных классов и методов позволяет описать некий шаблон объекта, который должен быть реализован в других классах. В них же самих описывается лишь некое общее для всех потомков поведение.

[to the top](#java-core)

## Could you explain term `interface`. What access modifiers methods and fields of interface usually have?
In Java, an interface is an abstract type that contains a collection of methods and constant variables. 
It is one of the core concepts in Java and is used to achieve abstraction, polymorphism and multiple inheritances.
The main purpose of an interface is to define how you can use class which implements this interface
Creator of an interface defines methods' names, types of method arguments and return types, but often doesn't implement them
(except for `default` and `static` interface methods which were introduced in java 8)   
All methods are implicitly `public`.

Interface can contain fields, in this case they declared as `public static final`.

[to the top](#java-core)

## What is the difference between abstract class and interface? In which scenario it is more appropriate to use an abstract class rather than the interface(s)?
+ Abstract class doesn't support multiple inheritance, interface supports multiple inheritance(only from other interfaces).
+ Abstract classes are used only when the "is a" relationship type is present. Interfaces can be implemented by classes that are not related to each other.
+ Abstract class can have abstract and non-abstract methods. Interface can have only abstract methods. Since Java 8, it can have `default`, `static`, `private`, `private static` methods also.
+ An abstract class is a means to avoid writing repetitive code, a tool for partially implementing behavior.
  An interface is a means of expressing the semantics of a class, a contract describing the capabilities. All interface methods
implicitly declared as `public abstract` or(started from java 8) `default`/`static` - methods with some implementation and fields implicitly declared as `public static final`.
+ Interfaces allow to create types structures without hierarchy.
+ An abstract class can extend another Java class and implement multiple Java interfaces. An interface can extend another Java interface only.

Abstract classes contain 

Abstract classes contain a partial implementation that is complemented or extended in subclasses.
At the same time, all subclasses are similar to each other in terms of the implementation inherited from the abstract class,
and differ only in terms of their own implementation of the abstract methods of the parent.
Therefore, abstract classes are used in the case of building a hierarchy of the same type, very similar to each other classes.
In this case, inheriting from an abstract class that implements the default behavior of an object can be useful, as it avoids
writing repetitive code. In all other cases, it is better to use interfaces.

[to the top](#java-core)

## Why some interfaces don't define methods at all?
A marker interface is an interface that doesn’t have any methods or constants inside it. 
It provides run-time type information about objects, so the compiler and JVM have additional information about the object.
For example, interface `Clonable`, which indicates that the class supports the cloning mechanism.

[to the top](#java-core)

## Почему нельзя объявить метод интерфейса с модификатором `final`?
В случае интерфейсов указание модификатора `final` бессмысленно, т.к. все методы интерфейсов неявно объявляются как абстрактные, т.е. их невозможно выполнить, не реализовав где-то еще, а этого нельзя будет сделать, если у метода идентификатор `final`.

[to the top](#java-core)

## Что имеет более высокий уровень абстракции - _класс_, _абстрактный класс_ или _интерфейс_?
Интерфейс.

[to the top](#java-core)

## Может ли объект получить доступ к члену класса, объявленному как `private`? Если да, то каким образом?
+ Внутри класса доступ к приватной переменной открыт без ограничений;
+ Вложенный класс имеет полный доступ ко всем (в том числе и приватным) членам содержащего его класса;
+ Доступ к приватным переменным извне может быть организован через отличные от приватных методов, которые предоставлены разработчиком класса. Например: `getX()` и `setX()`.
+ Через механизм рефлексии (Reflection API):

```java
class Victim { 
    private int field = 42;
}
//...
Victim victim = new Victim(); 
Field field = Victim.class.getDeclaredField("field"); 
field.setAccessible(true); 
int fieldValue = (int) field.get(victim);
//...
```

[to the top](#java-core)

## Каков порядок вызова конструкторов и блоков инициализации с учётом иерархии классов?
Сначала вызываются все статические блоки в очередности от первого статического блока корневого предка и выше по цепочке иерархии до статических блоков самого класса. 

Затем вызываются нестатические блоки инициализации корневого предка, конструктор корневого предка и так далее вплоть до нестатических блоков и конструктора самого класса.

>Parent static block(s) → Child static block(s) → Grandchild static block(s)
>
> → Parent non-static block(s) → Parent constructor →
>
> → Child non-static block(s) → Child constructor →
>
> → Grandchild non-static block(s) → Grandchild constructor

Пример 1:

```java
public class MainClass {

    public static void main(String args[]) {
        System.out.println(TestClass.v);
        new TestClass().a();
    }

}
```

```java
public class TestClass {

    public static String v = "Some val";

    {
        System.out.println("!!! Non-static initializer");
    }

    static {
        System.out.println("!!! Static initializer");
    }

    public void a() {
        System.out.println("!!! a() called");
    }

}
```

Результат выполнения:

```
!!! Static initializer
Some val
!!! Non-static initializer
!!! a() called
```

Пример 2:

```java
public class MainClass {

    public static void main(String args[]) {        
        new TestClass().a();
    }

}
```

```java
public class TestClass {

    public static String v = "Some val";

    {
        System.out.println("!!! Non-static initializer");
    }

    static {
        System.out.println("!!! Static initializer");
    }

    public void a() {
        System.out.println("!!! a() called");
    }

}
```

Результат выполнения:

```
!!! Static initializer
!!! Non-static initializer
!!! a() called
```

[to the top](#java-core)

## Зачем нужны и какие бывают блоки инициализации?
Блоки инициализации представляют собой код, заключенный в фигурные скобки и размещаемый внутри класса вне объявления методов или конструкторов. 

+ Существуют статические и нестатические блоки инициализации.
+ Блок инициализации выполняется перед инициализацией класса загрузчиком классов или созданием объекта класса с помощью конструктора. 
+ Несколько блоков инициализации выполняются в порядке следования в коде класса. 
+ Блок инициализации способен генерировать исключения, если их объявления перечислены в `throws` всех конструкторов класса.
+ Блок инициализации возможно создать и в анонимном классе.

[to the top](#java-core)

## К каким конструкциям Java применим модификатор `static`?
+ полям;
+ методам;
+ вложенным классам;
+ блокам инициализации;
+ членам секции `import`.

[to the top](#java-core)

## Для чего в Java используются статические блоки инициализации?
Статические блоки инициализация используются для выполнения кода, который должен выполняться один раз при инициализации класса загрузчиком классов, в момент, предшествующий созданию объектов этого класса при помощи конструктора. Такой блок (в отличие от нестатических, принадлежащих конкретном объекту класса) принадлежит только самому классу (объекту метакласса `Class`).

[to the top](#java-core)

## Что произойдёт, если в блоке инициализации возникнет исключительная ситуация?
Для нестатических блоков инициализации, если выбрасывание исключения прописано явным образом требуется, чтобы объявления этих исключений были перечислены в `throws` всех конструкторов класса. Иначе будет ошибка компиляции. Для статического блока выбрасывание исключения в явном виде, приводит к ошибке компиляции.

В остальных случаях, взаимодействие с исключениями будет проходить так же, как и в любом другом месте. Класс не будет инициализирован, если ошибка происходит в статическом блоке и объект класса не будет создан, если ошибка возникает в нестатическом блоке.

[to the top](#java-core)

## Какое исключение выбрасывается при возникновении ошибки в блоке инициализации класса?
Если возникшее исключение - наследник `RuntimeException`:

+ для статических блоков инициализации будет выброшено `java.lang.ExceptionInInitializerError`;
+ для нестатических будет проброшено исключение-источник.

Если возникшее исключение - наследник `Error`, то в обоих случаях будет выброшено `java.lang.Error`. Исключение: `java.lang.ThreadDeath` - смерть потока. В этом случае никакое исключение выброшено не будет.

[to the top](#java-core)

## Может ли статический метод быть переопределён или перегружен?
Перегружен - да. Всё работает точно так же, как и с обычными методами - 2 статических метода могут иметь одинаковое имя, если количество их параметров или типов различается. 

Переопределён - нет. Выбор вызываемого статического метода происходит при раннем связывании (на этапе компиляции, а не выполнения) и выполняться всегда будет родительский метод, хотя синтаксически переопределение статического метода - это вполне корректная языковая конструкция.

В целом, к статическим полям и методам рекомендуется обращаться через имя класса, а не объект.

[to the top](#java-core)

## Могут ли нестатические методы перегрузить статические?
Да. В итоге получится два разных метода. Статический будет принадлежать классу и будет доступен через его имя, а нестатический будет принадлежать конкретному объекту и доступен через вызов метода этого объекта.

[to the top](#java-core)

## Is Java "pass-by-reference" or "pass-by-value"?
Pass-by-value means that the _value_ of a variable is passed to a function/method. 
Pass-by-reference means that a _reference_ to variable is passed to the function

By those definitions java is always **pass-by-value**. But in java when you deal with variables 
holding objects we are really dealing with object handlers called _references_ which are passed-by-value as 
well.
You can see it via example.
```java
public static void main(String[] args) {
        Dog aDog = new Dog("Max");
        Dog oldDog = aDog;

        // we pass the object to foo
        foo(aDog);
        // aDog variable is still pointing to the "Max" dog when foo(...) returns
        aDog.getName().equals("Max"); // true
        aDog.getName().equals("Fifi"); // false
        aDog == oldDog; // true
        }

public static void foo(Dog d) {
        d.getName().equals("Max"); // true
        // change d inside of foo() to point to a new Dog instance "Fifi"
        d = new Dog("Fifi");
        d.getName().equals("Fifi"); // true
        }
```
In this example we see that `aDog.getName()` still returns `Max`. The value `aDog` is not changed in the function
`foo` with the Dog `"Fifi"` as the object reference is passed by value. If it were passed by reference, 
then the `aDog.getName()` in main would return `"Fifi"` after the call of `foo`. 

```java
public static void main(String[] args) {
    Dog aDog = new Dog("Max");
    Dog oldDog = aDog;

    // we pass the object to foo
    foo(aDog);
    // aDog variable is still pointing to the "Max" dog when foo(...) returns
    aDog.getName().equals("Max"); // true
    aDog.getName().equals("Fifi"); // false
    aDog == oldDog; // true
}

public static void foo(Dog d) {
    d.getName().equals("Max"); // true
    // change d inside of foo() to point to a new Dog instance "Fifi"
    d = new Dog("Fifi");
    d.getName().equals("Fifi"); // true
}
```
In this example, `Fifi` is the dog's name after call `foo(aDog)` because the object's name was set inside
of `foo(..)` 

[stackoverflow 1](https://stackoverflow.com/a/40523/22463602)
[stackoverflow 2](https://stackoverflow.com/a/430958/22463602)

[to the top](#java-core)

## Можно ли сузить уровень доступа/тип возвращаемого значения при переопределении метода?

+ При переопределении метода нельзя сузить модификатор доступа к методу (например с public в MainClass до private в Class extends MainClass). 
+ Изменить тип возвращаемого значения при переопределении метода нельзя, будет ошибка attempting to use incompatible return type. 
+ Можно сузить возвращаемое значение, если они совместимы. 

Например:

```java
public class Animal {

    public Animal eat() {
        System.out.println("animal eat");
        return null;
    }
    
    public Long calc() {
        return null;
    }

}
public class Dog extends Animal {

    public Dog eat() {
        return new Dog();
    }
/*attempting to use incompatible return type
    public Integer calc() {
        return null;
    }
*/
}
```

## Возможно ли при переопределении метода изменить: модификатор доступа, возвращаемый тип, тип аргумента или их количество, имена аргументов или их порядок; убирать, добавлять, изменять порядок следования элементов секции `throws`?
При переопределении метода сужать модификатор доступа не разрешается, т.к. это приведёт к нарушению принципа подстановки Барбары Лисков. Расширение уровня доступа возможно.

Можно изменять все, что не мешает компилятору понять какой метод родительского класса имеется в виду:

+ Изменять тип возвращаемого значения при переопределении метода разрешено только в сторону сужения типа (вместо родительского класса - наследника).
+ При изменении типа, количества, порядка следования аргументов вместо переопределения будет происходить _overloading_ (перегрузка) метода.
+ Секцию `throws` метода можно не указывать, но стоит помнить, что она остаётся действительной, если уже определена у метода родительского класса. Так же, возможно добавлять новые исключения, являющиеся наследниками от уже объявленных или исключения `RuntimeException`. Порядок следования таких элементов при переопределении значения не имеет.

[to the top](#java-core)

## Как получить доступ к переопределенным методам родительского класса?
С помощью ключевого слова `super` мы можем обратиться к любому члену родительского класса - методу или полю, если они не определены с модификатором `private`.

```java
super.method();
```

[to the top](#java-core)

## Можно ли объявить метод абстрактным и статическим одновременно?
Нет. В таком случае компилятор выдаст ошибку: _"Illegal combination of modifiers: ‘abstract’ and ‘static’"_. Модификатор `abstract` говорит, что метод будет реализован в другом классе, а `static` наоборот указывает, что этот метод будет доступен по имени класса.

[to the top](#java-core)

## В чем разница между членом экземпляра класса и статическим членом класса?
Модификатор `static` говорит о том, что данный метод или поле принадлежат самому классу и доступ к ним возможен даже без создания экземпляра класса. Поля, помеченные `static` инициализируются при инициализации класса. На методы, объявленные как `static`, накладывается ряд ограничений:

+ Они могут вызывать только другие статические методы.
+ Они должны осуществлять доступ только к статическим переменным.
+ Они не могут ссылаться на члены типа `this` или `super`.

В отличии от статических, поля экземпляра класса принадлежат конкретному объекту и могут иметь разные значения для каждого. Вызов метода экземпляра возможен только после предварительного создания объекта класса.

Пример:
```java
public class MainClass {

	public static void main(String args[]) {
		System.out.println(TestClass.v);
		new TestClass().a();
		System.out.println(TestClass.v);
	}

}
```

```java
public class TestClass {

	public static String v = "Initial val";

	{
		System.out.println("!!! Non-static initializer");
		v = "Val from non-static";
	}

	static {
		System.out.println("!!! Static initializer");
		v = "Some val";
	}

	public void a() {
		System.out.println("!!! a() called");
	}

}
```

Результат:

```
!!! Static initializer
Some val
!!! Non-static initializer
!!! a() called
Val from non-static

```

[to the top](#java-core)

## Где разрешена инициализация статических/нестатических полей?
+ Статические поля можно инициализировать при объявлении, в статическом или нестатическом блоке инициализации. 
+ Нестатические поля можно инициализировать при объявлении, в нестатическом блоке инициализации или в конструкторе.

[to the top](#java-core)

## What types of classes are exist in java?
+ _Top level class_:
    + _Abstract class_ 
    + _Final class_ 
    + _Record class_
+ _Interfaces_ 
+ _Enum_ 
+ _Nested class_ 
    + _Static nested class_ 
    + _Member inner class_ 
    + _Local inner class_ 
    + _Anonymous inner class_

[to the top](#java-core)

## Are java classes objects of `Class<T>`? 

A Java class is not an object.

However, every Java class has an instance of the `Class class` describing it.
Those instances are objects

[StackOverflow](https://stackoverflow.com/a/11990306/22463602)

## Расскажите про вложенные классы. В каких случаях они применяются?
Класс называется вложенным (_Nested class_), если он определен внутри другого класса. Вложенный класс должен создаваться только для того, чтобы обслуживать обрамляющий его класс. Если вложенный класс оказывается полезен в каком-либо ином контексте, он должен стать классом верхнего уровня. Вложенные классы имеют доступ ко всем (в том числе приватным) полям и методам внешнего класса, но не наоборот. Из-за этого разрешения использование вложенных классов приводит к некоторому нарушению инкапсуляции.

Существуют четыре категории вложенных классов: 
+ _Static nested class_ (Статический вложенный класс);
+ _Member inner class_ (Простой внутренний класс);
+ _Local inner class_ (Локальный класс);
+ _Anonymous inner class_ (Анонимный класс).

Такие категории классов, за исключением первого, также называют внутренними (_Inner class_). Внутренние классы ассоциируются не с внешним классом, а с экземпляром внешнего.

Каждая из категорий имеет рекомендации по своему применению. Если вложенный класс должен быть виден за пределами одного метода или он слишком длинный для того, чтобы его можно было удобно разместить в границах одного метода и если каждому экземпляру такого класса необходима ссылка на включающий его экземпляр, то используется нестатический внутренний класс. В случае, если ссылка на обрамляющий класс не требуется - лучше сделать такой класс статическим. Если класс необходим только внутри какого-то метода и требуется создавать экземпляры этого класса только в этом методе, то используется локальный класс. А, если к тому же применение класса сводится к использованию лишь в одном месте и уже существует тип, характеризующий этот класс, то рекомендуется делать его анонимным классом.

[to the top](#java-core)

## Что такое _«статический класс»_?
Это вложенный класс, объявленный с использованием ключевого слова `static`. К классам верхнего уровня модификатор `static` неприменим.

[to the top](#java-core)

## Какие существуют особенности использования вложенных классов: статических и внутренних? В чем заключается разница между ними?

+ Вложенные классы могут обращаться ко всем членам обрамляющего класса, в том числе и приватным. 
+ Для создания объекта статического вложенного класса объект внешнего класса не требуется.
+ Из объекта статического вложенного класса нельзя обращаться к не статическим членам обрамляющего класса напрямую, а только через ссылку на экземпляр внешнего класса.
+ Обычные вложенные классы не могут содержать статических методов, блоков инициализации и классов. Статические вложенные классы - могут.
+ В объекте обычного вложенного класса хранится ссылка на объект внешнего класса. Внутри статической такой ссылки нет. Доступ к экземпляру обрамляющего класса осуществляется через указание `.this` после его имени. Например: `Outer.this`.

[to the top](#java-core)

## Что такое _«локальный класс»_? Каковы его особенности?
__Local inner class__ (Локальный класс) - это вложенный класс, который может быть декларирован в любом блоке, в котором разрешается декларировать переменные. Как и простые внутренние классы (_Member inner class_) локальные классы имеют имена и могут использоваться многократно. Как и анонимные классы, они имеют окружающий их экземпляр только тогда, когда применяются в нестатическом контексте.

Локальные классы имеют следующие особенности:

+ Видны только в пределах блока, в котором объявлены;
+ Не могут быть объявлены как `private`/`public`/`protected` или `static`;
+ Не могут иметь внутри себя статических объявлений методов и классов, но могут иметь финальные статические поля, проинициализированные константой;
+ Имеют доступ к полям и методам обрамляющего класса;
+ Могут обращаться к локальным переменным и параметрам метода, если они объявлены с модификатором `final`.

[to the top](#java-core)

## Что такое _«анонимные классы»_? Где они применяются?
Это вложенный локальный класс без имени, который разрешено декларировать в любом месте обрамляющего класса, разрешающем размещение выражений. Создание экземпляра анонимного класса происходит одновременно с его объявлением. В зависимости от местоположения анонимный класс ведет себя как статический либо как нестатический вложенный класс - в нестатическом контексте появляется окружающий его экземпляр.

Анонимные классы имеют несколько ограничений:

+ Их использование разрешено только в одном месте программы - месте его создания;
+ Применение возможно только в том случае, если после порождения экземпляра нет необходимости на него ссылаться;
+ Реализует лишь методы своего интерфейса или суперкласса, т.е. не может объявлять каких-либо новых методов, так как для доступа к ним нет поименованного типа.

Анонимные классы обычно применяются для: 

+ создания объекта функции (_function object_), например, реализация интерфейса `Comparator`;
+ создания объекта процесса (_process object_), такого как экземпляры классов `Thread`, `Runnable` и подобных;
+ в статическом методе генерации;
+ инициализации открытого статического поля `final`, которое соответствует сложному перечислению типов, когда для каждого экземпляра в перечислении требуется отдельный подкласс.

[to the top](#java-core)

## Каким образом из вложенного класса получить доступ к полю внешнего класса?
Статический вложенный класс имеет прямой доступ только к статическим полям обрамляющего класса. 

Простой внутренний класс, может обратиться к любому полю внешнего класса напрямую. В случае, если у вложенного класса уже существует поле с таким же литералом, то обращаться к такому полю следует через ссылку на его экземпляр. Например: `Outer.this.field`.

[to the top](#java-core)

## Для чего используется оператор `assert`?
__Assert__ (Утверждение) — это специальная конструкция, позволяющая проверять предположения о значениях произвольных данных в произвольном месте программы. Утверждение может автоматически сигнализировать об обнаружении некорректных данных, что обычно приводит к аварийному завершению программы с указанием места обнаружения некорректных данных.

Утверждения существенно упрощают локализацию ошибок в коде. Даже проверка результатов выполнения очевидного кода может оказаться полезной при последующем рефакторинге, после которого код может стать не настолько очевидным и в него может закрасться ошибка. 

Обычно утверждения оставляют включенными во время разработки и тестирования программ, но отключают в релиз-версиях программ.

Т.к. утверждения могут быть удалены на этапе компиляции либо во время исполнения программы, они не должны менять поведение программы. Если в результате удаления утверждения поведение программы может измениться, то это явный признак неправильного использования _assert_. Таким образом, внутри _assert_ нельзя вызывать методы, изменяющие состояние программы, либо внешнего окружения программы. 

В Java проверка утверждений реализована с помощью оператора `assert`, который имеет форму:

`assert [Выражение типа boolean];` или `assert [Выражение типа boolean] : [Выражение любого типа, кроме void];`

Во время выполнения программы в том случае, если поверка утверждений включена, вычисляется значение булевского выражения, и если его результат `false`, то генерируется исключение `java.lang.AssertionError`. В случае использования второй формы оператора `assert` выражение после двоеточия задаёт детальное сообщение о произошедшей ошибке (вычисленное выражение будет преобразовано в строку и передано конструктору `AssertionError`).

[to the top](#java-core)

## What are _Heap_ and _Stack_ memory in Java? What's the difference between them?
__Heap__ is used by Java Runtime memory allocation to storing objects.
Garbage collected area is heap.
Any object which is created in heap have a global access and it might be referenced from any part of the application.

__Stack (стек)__ это область хранения данных также находящееся в общей оперативной памяти (_RAM_). Whenever a method is called,
a new block is created in the stack memory, which contains primitives and references to other objects in the method.
As soon as the method finishes working, the block also stops being used, thereby providing access for the next method.
The size of the stack memory is much smaller than the amount of memory in the heap. The stack in Java works according to the scheme _LIFO_ (Last in, first out)

Both _stack_ and _heap_ are stored in RAM.

Различия между _Heap_ и _Stack_ памятью:
+ The entire application uses Heap space during runtime. Stack is used in parts, one at a time during execution of a thread
+ All the newly created objects are stored in heap, stack stores only primitive variables and references to objects that are created in Heap Space
+ Objects in heap are available from any part of the program, while stack memory can't be accessed from other threads.
+ Stack memory only exists as long as the current method is running, Heap space exists as long as the application runs.
+ If stack memory is full then Java Runtime throws exception `java.lang.StackOverflowError`. If heap is out of memory, then `java.lang.OutOfMemoryError: Java Heap Space` is thrown.
+ Stack has less memory than heap 
+ Stack is much faster to allocate when compared to heap(because allocate memory in stack much easier)

The `-Xms` and `-Xmx` JVM options are used to determine the initial and maximum memory size in the heap.
For the stack, you can determine the memory size using the `-Xss` option.

[to the top](#java-core)

## Верно ли утверждение, что примитивные типы данных всегда хранятся в стеке, а экземпляры ссылочных типов данных в куче?
Не совсем. Примитивное поле экземпляра класса хранится не в стеке, а в куче. Любой объект (всё, что явно или неявно создаётся при помощи оператора `new`) хранится в куче.

[to the top](#java-core)

## Каким образом передаются переменные в методы, по значению или по ссылке?
В Java параметры всегда передаются только по значению, что определяется как «скопировать значение и передать копию». С примитивами это будет копия содержимого. Со ссылками - тоже копия содержимого, т.е. копия ссылки. При этом внутренние члены ссылочных типов через такую копию изменить возможно, а вот саму ссылку, указывающую на экземпляр - нет.

[to the top](#java-core)

## Для чего нужен сборщик мусора?
Сборщик мусора (Garbage Collector) должен делать всего две вещи:

+ Находить мусор - неиспользуемые объекты. (Объект считается неиспользуемым, если ни одна из сущностей в коде, выполняемом в данный момент, не содержит ссылок на него, либо цепочка ссылок, которая могла бы связать объект с некоторой сущностью приложения, обрывается);
+ Освобождать память от мусора.

Существует два подхода к обнаружению мусора:

+ _Reference counting_;
+ _Tracing_

__Reference counting__ (подсчёт ссылок). Суть этого подхода состоит в том, что каждый объект имеет счетчик. Счетчик хранит информацию о том, сколько ссылок указывает на объект. Когда ссылка уничтожается, счетчик уменьшается. Если значение счетчика равно нулю, - объект можно считать мусором. Главным минусом такого подхода является сложность обеспечения точности счетчика. Также при таком подходе сложно выявлять циклические зависимости (когда два объекта указывают друг на друга, но ни один живой объект на них не ссылается), что приводит к утечкам памяти.

Главная идея подхода __Tracing__ (трассировка) состоит в утверждении, что живыми могут считаться только те объекты, до которых мы можем добраться из корневых точек (_GC Root_) и те объекты, которые доступны с живого объекта. Всё остальное - мусор.

Существует 4 типа корневых точки:

+ Локальные переменные и параметры методов;
+ Потоки;
+ Статические переменные;
+ Ссылки из JNI.

Самое простое java приложение будет иметь корневые точки:

+ Локальные переменные внутри `main()` метода и параметры `main()` метода;
+ Поток который выполняет `main()`;
+ Статические переменные класса, внутри которого находится `main()` метод.

Таким образом, если мы представим все объекты и ссылки между ними как дерево, то нам нужно будет пройти с корневых узлов (точек) по всем рёбрам. При этом узлы, до которых мы сможем добраться - не мусор, все остальные - мусор. При таком подходе циклические зависимости легко выявляются. HotSpot VM использует именно такой подход.

---
Для очистки памяти от мусора существуют два основных метода:

+ _Copying collectors_
+ _Mark-and-sweep_

При __copying collectors__ подходе память делится на две части «from-space» и «to-space», при этом сам принцип работы такой:

+ Объекты создаются в «from-space»;
+ Когда «from-space» заполняется, приложение приостанавливается;
+ Запускается сборщик мусора. Находятся живые объекты в «from-space» и копируются в «to-space»;
+ Когда все объекты скопированы «from-space» полностью очищается;
+ «to-space» и «from-space» меняются местами.

Главный плюс такого подхода в том, что объекты плотно забивают память. Минусы подхода:

1. Приложение должно быть остановлено на время, необходимое для полного прохождения цикла сборки мусора;
2. В худшем случае (когда все объекты живые) «form-space» и «to-space» будут обязаны быть одинакового размера.

Алгоритм работы __mark-and-sweep__ можно описать так:

+ Объекты создаются в памяти;
+ В момент, когда нужно запустить сборщик мусора приложение приостанавливается;
+ Сборщик проходится по дереву объектов, помечая живые объекты;
+ Сборщик проходится по всей памяти, находя все не отмеченные куски памяти и сохраняя их в «free list»;
+ Когда новые объекты начинают создаваться они создаются в памяти доступной во «free list».

Минусы этого способа:

1. Приложение не работает пока происходит сборка мусора;
2. Время остановки напрямую зависит от размеров памяти и количества объектов;
3. Если не использовать «compacting» память будет использоваться не эффективно.

Сборщики мусора HotSpot VM используют комбинированный подход __Generational Garbage Collection__, который позволяет использовать разные алгоритмы для разных этапов сборки мусора. Этот подход опирается на том, что:

+ большинство создаваемых объектов быстро становятся мусором;
+ существует мало связей между объектами, которые были созданы в прошлом и только что созданными объектами.

[to the top](#java-core)

## Как работает сборщик мусора?
Механизм сборки мусора - это процесс освобождения места в куче, для возможности добавления новых объектов.

Объекты создаются посредством оператора `new`, тем самым присваивая объекту ссылку. Для окончания работы с объектом достаточно просто перестать на него ссылаться, например, присвоив переменной ссылку на другой объект или значение `null`; прекратить выполнение метода, чтобы его локальные переменные завершили свое существование естественным образом. Объекты, ссылки на которые отсутствуют, принято называть мусором (_garbage_), который будет удален.

Виртуальная машина Java, применяя механизм сборки мусора, гарантирует, что любой объект, обладающий ссылками, остается в памяти — все объекты, которые недостижимы из исполняемого кода, ввиду отсутствия ссылок на них, удаляются с высвобождением отведенной для них памяти. Точнее говоря, объект не попадает в сферу действия процесса сборки мусора, если он достижим посредством цепочки ссылок, начиная с корневой (_GC Root_) ссылки, т.е. ссылки, непосредственно существующей в выполняемом коде.

Память освобождается сборщиком мусора по его собственному «усмотрению». Программа может успешно завершить работу, не исчерпав ресурсов свободной памяти или даже не приблизившись к этой черте и поэтому ей так и не потребуются «услуги» сборщика мусора.

Мусор собирается системой автоматически, без вмешательства пользователя или программиста, но это не значит, что этот процесс не требует внимания вовсе. Необходимость создания и удаления большого количества объектов существенным образом сказывается на производительности приложений и, если быстродействие программы является важным фактором, следует тщательно обдумывать решения, связанные с созданием объектов, — это, в свою очередь, уменьшит и объем мусора, подлежащего утилизации.

[to the top](#java-core)

## What types of Garbage collectors exist in HotSpot JVM?
Java HotSpot VM has 5 types of garbage collectors.

+ __Serial GC__ — Used where just one thread executed the GC, freezes all app threads when working, to use it, execute: `-XX:+UseSerialGC`.
+ __Parallel GC__ — Used where multiple minor threads are executed simultaneously, also freezes all app threads, 
if you want to use it: `-XX:+UseParallelGC`.
+ __Concurrent Mark Sweep (CMS)__ —  Similar to parallel, reduces stop-the-world paused. 
Has 2 phases **Mark phase and Sweep phase**, _mark phase_ mark all live objects and executes in multiple threads, it stops all app threads, 
_sweep phase_ run simultaneously with app threads, but because of this uses more CPU, to activate: `-XX:+UseConcMarkSweepGC`.
+ __Garbage-First (G1)__ — Used when we have large heap(>4gb). It partitions heap into set of equal size
regions and uses multiple threads to scan them and mark objects as live or dead,
after marking G1 knows which regions contains the most garbage and sweeps them. 
Works concurrently with the app. To use it: `-XX:+UseG1GC`.
+ **Z Garbage collector** was introduced in java 11 and in java 15 set to default. Highly scalable and low-latency GC. 
Performs very expensive tasks concurrently without stopping the world, to use it: `-XX:+UseZGC`

[to the top](#java-core)

## Опишите алгоритм работы какого-нибудь сборщика мусора, реализованного в виртуальной машине HotSpot.
__Serial Garbage Collector (Последовательный сборщик мусора)__ был одним из первых сборщиков мусора в HotSpot VM. Во время работы этого сборщика приложения приостанавливается и продолжает работать только после прекращения сборки мусора. 

Память приложения делится на три пространства:

+ _Young generation_. Объекты создаются именно в этом участке памяти.
+ _Old generation_. В этот участок памяти перемещаются объекты, которые переживают «minor garbage collection».
+ _Permanent generation_. Тут хранятся метаданные об объектах, _Class data sharing (CDS)_, _пул строк (String pool)_. Permanent область делится на две: только для чтения и для чтения-записи. Очевидно, что в этом случае область только для чтения не чистится сборщиком мусора никогда.

Область памяти Young generation состоит из трёх областей: _Eden_ и двух меньших по размеру _Survivor spaces_ - _To space_ и _From space_. Большинство объектов создаются в области Eden, за исключением очень больших объектов, которые не могут быть размещены в ней и поэтому сразу размещаются в Old generation. В Survivor spaces перемещаются объекты, которые пережили по крайней мере одну сборку мусора, но ещё не достигли порога «старости» (_tenuring threshold_), чтобы быть перемещенными в Old generation.

Когда Young generation заполняется, то в этой области запускается процесс лёгкой сборки (_minor collection_), в отличие от процесса сборки, проводимого над всей кучей (_full collection_). Он происходит следующим образом: в начале работы одно из Survivor spaces - To space, является пустым, а другое - From space, содержит объекты, пережившие предыдущие сборки. Сборщик мусора ищет живые объекты в Eden и копирует их в To space, а затем копирует туда же и живые «молодые» (то есть не пережившие еще заданное число сборок мусора) объекты из From space. Старые объекты из From space перемещаются в Old generation. После лёгкой сборки From space и To space меняются ролями, область Eden становится пустой, а число объектов в Old generation увеличивается.

Если в процессе копирования живых объектов To space переполняется, то оставшиеся живые объекты из Eden и From space, которым не хватило места в To space, будут перемещены в Old generation, независимо от того, сколько сборок мусора они пережили.

Поскольку при использовании этого алгоритма сборщик мусора просто копирует все живые объекты из одной области памяти в другую, то такой сборщик мусора называется _copying_ (копирующий). Очевидно, что для работы копирующего сборщика мусора у приложения всегда должна быть свободная область памяти, в которую будут копироваться живые объекты, и такой алгоритм может применяться для областей памяти сравнительно небольших по отношению к общему размеру памяти приложения. Young generation как раз удовлетворяет этому условию (по умолчанию на машинах клиентского типа эта область занимает около 10% кучи (значение может варьироваться в зависимости от платформы)).

Однако, для сборки мусора в Old generation, занимающем большую часть всей памяти, используется другой алгоритм.

В Old generation сборка мусора происходит с использованием алгоритма _mark-sweep-compact_, который состоит из трёх фаз. В фазе _Mark_ (пометка) сборщик мусора помечает все живые объекты, затем, в фазе _Sweep_ (очистка) все не помеченные объекты удаляются, а в фазе _Сompact_ (уплотнение) все живые объекты перемещаются в начало Old generation, в результате чего свободная память после очистки представляет собой непрерывную область. Фаза уплотнения выполняется для того, чтобы избежать фрагментации и упростить процесс выделения памяти в Old generation.

Когда свободная память представляет собой непрерывную область, то для выделения памяти под создаваемый объект можно использовать очень быстрый (около десятка машинных инструкций) алгоритм _bump-the-pointer_: адрес начала свободной памяти хранится в специальном указателе, и когда поступает запрос на создание нового объекта, код проверяет, что для нового объекта достаточно места, и, если это так, то просто увеличивает указатель на размер объекта.

Последовательный сборщик мусора отлично подходит для большинства приложений, использующих до 200 мегабайт кучи, работающих на машинах клиентского типа и не предъявляющих жёстких требований к величине пауз, затрачиваемых на сборку мусора. В то же время модель «stop-the-world» может вызвать длительные паузы в работе приложения при использовании больших объёмов памяти. Кроме того, последовательный алгоритм работы не позволяет оптимально использовать вычислительные ресурсы компьютера, и последовательный сборщик мусора может стать узким местом при работе приложения на многопроцессорных машинах.

[to the top](#java-core)

## Describe most popular memory switches to tune heap

[//]: # (TODO)

[to the top](#java-core)

## What is string pool in java?
**String pool** is a storage space in the Java heap memory where string literals are stored. It is also known as String Constant Pool or String Intern Pool

+ String pool is possible due to the immutability of strings in Java and the implementation of the idea of interning strings;
+ A string pool helps save memory, but for the same reason, creating a string takes longer;
+ When `"` is used to create a string, then first a string in the pool with the same value is searched, 
if it is found, then a link is returned, otherwise a new string is created in the pool, and then a link to it is returned;
+ When using the `new` operator, a new `String` object is created. Then, using the `intern()` method, this string can be placed in a pool or
  get a reference from the pool to another `String` object with the same value;
+ String pool is an example of _Flyweight_ design pattern.

[to the top](#java-core)

## Что такое `finalize()`? Зачем он нужен?
Через вызов метода `finalize()` (который наследуется от Java.lang.Object) JVM реализуется функциональность аналогичная функциональности деструкторов в С++, используемых для очистки памяти перед возвращением управления операционной системе. Данный метод вызывается при уничтожении объекта сборщиком мусора (_garbage collector_) и переопределяя `finalize()` можно запрограммировать действия необходимые для корректного удаления экземпляра класса - например, закрытие сетевых соединений, соединений с базой данных, снятие блокировок на файлы и т.д. 

После выполнения этого метода объект должен быть повторно собран сборщиком мусора (и это считается серьезной проблемой метода `finalize()` т.к. он мешает сборщику мусора освобождать память). Вызов этого метода не гарантируется, т.к. приложение может быть завершено до того, как будет запущена сборка мусора.

Объект не обязательно будет доступен для сборки сразу же - метод `finalize()` может сохранить куда-нибудь ссылку на объект. Подобная ситуация называется «возрождением» объекта и считается антипаттерном. Главная проблема такого трюка - в том, что «возродить» объект можно только 1 раз.

Пример:
```java
public class MainClass {

	public static void main(String args[]) {
		TestClass a = new TestClass();
		a.a();
		a = null;
		a = new TestClass();
		a.a();
		System.out.println("!!! done");
	}
}
```
```java

public class TestClass {

	public void a() {
		System.out.println("!!! a() called");
	}

	@Override
	protected void finalize() throws Throwable {
		System.out.println("!!! finalize() called");
		super.finalize();
	}
}
```
Так как в данном случае сборщик мусора может и не быть вызван (в силу простоты приложения), то результат выполнения программы с большой вероятностью будет следующий:
```
!!! a() called
!!! a() called
!!! done
```
Теперь несколько усложним программу, добавив принудительный вызов Garbage Collector:
```java
public class MainClass {

	public static void main(String args[]) {
		TestClass a = new TestClass();
		a.a();
		a = null;
		System.gc(); // Принудительно зовём сборщик мусора
		a = new TestClass();
		a.a();
		System.out.println("!!! done");
	}

}
```
Как и было сказано ранее, Garbage Collector может в разное время отработать, поэтому результат выполнения может разниться от запуска к запуску:
Вариант а:
```
!!! a() called
!!! a() called
!!! done
!!! finalize() called
```
Вариант б:
```
!!! a() called
!!! a() called
!!! finalize() called
!!! done
```


[to the top](#java-core)

## Что произойдет со сборщиком мусора, если выполнение метода `finalize()` требует ощутимо много времени, или в процессе выполнения будет выброшено исключение?
Непосредственно вызов `finalize()` происходит в отдельном потоке _Finalizer_ (`java.lang.ref.Finalizer.FinalizerThread`), который создаётся при запуске виртуальной машины (в статической секции при загрузке класса `Finalizer`). Методы `finalize()` вызываются последовательно в том порядке, в котором были добавлены в список сборщиком мусора. Соответственно, если какой-то `finalize()` зависнет, он подвесит поток _Finalizer_, но не сборщик мусора. Это в частности означает, что объекты, не имеющие метода `finalize()`, будут исправно удаляться, а вот имеющие будут добавляться в очередь, пока поток _Finalizer_ не освободится, не завершится приложение или не кончится память. 

То же самое применимо и выброшенным в процессе `finalize()` исключениям: метод `runFinalizer()` у потока _Finalizer_ игнорирует все исключения выброшенные в момент выполнения `finalize()`. Таким образом возникновение исключительной ситуации никак не скажется на работоспособности сборщика мусора.

[to the top](#java-core)

## Чем отличаются `final`, `finally` и `finalize()`?
Модификатор `final`:

+ Класс не может иметь наследников;
+ Метод не может быть переопределен в классах наследниках;
+ Поле не может изменить свое значение после инициализации;
+ Локальные переменные не могут быть изменены после присвоения им значения;
+ Параметры методов не могут изменять своё значение внутри метода.

Оператор `finally` гарантирует, что определенный в нём участок кода будет выполнен независимо от того, какие исключения были возбуждены и перехвачены в блоке `try-catch`.

Метод `finalize()` вызывается перед тем как сборщик мусора будет проводить удаление объекта.

Пример:
```java

public class MainClass {

	public static void main(String args[]) {
		TestClass a = new TestClass();
		System.out.println("result of a.a() is " + a.a());
		a = null;
		System.gc(); // Принудительно зовём сборщик мусора
		a = new TestClass();
		System.out.println("result of a.a() is " + a.a());
		System.out.println("!!! done");
	}

}
```

```java
public class TestClass {

	public int a() {
		try {
			System.out.println("!!! a() called");
			throw new Exception("");
		} catch (Exception e) {
			System.out.println("!!! Exception in a()");
			return 2;
		} finally {
			System.out.println("!!! finally in a() ");
		}
	}

	@Override
	protected void finalize() throws Throwable {
		System.out.println("!!! finalize() called");
		super.finalize();
	}
}
```

Результат выполнения:

```
!!! a() called
!!! Exception in a()
!!! finally in a() 
result of a.a() is 2
!!! a() called
!!! Exception in a()
!!! finally in a() 
!!! finalize() called
result of a.a() is 2
!!! done
```

[to the top](#java-core)

## Расскажите про приведение типов. Что такое понижение и повышение типа?
Java является строго типизированным языком программирования, а это означает, то что каждое выражение и каждая переменная имеет строго определенный тип уже на момент компиляции. Однако определен механизм _приведения типов (casting)_ - способ преобразования значения переменной одного типа в значение другого типа. 

В Java существуют несколько разновидностей приведения:

+ __Тождественное (identity)__. Преобразование выражения любого типа к точно такому же типу всегда допустимо и происходит автоматически.
+ __Расширение (повышение, upcasting) примитивного типа (widening primitive)__. Означает, что осуществляется переход от менее емкого типа к более ёмкому. Например, от типа `byte` (длина 1 байт) к типу `int` (длина 4 байта). Такие преобразование безопасны в том смысле, что новый тип всегда гарантировано вмещает в себя все данные, которые хранились в старом типе и таким образом не происходит потери данных. Этот тип приведения всегда допустим и происходит автоматически.
+ __Сужение (понижение, downcasting) примитивного типа (narrowing primitive)__. Означает, что переход осуществляется от более емкого типа к менее емкому. При таком преобразовании есть риск потерять данные. Например, если число типа `int` было больше `127`, то при приведении его к `byte` значения битов старше восьмого будут потеряны. В Java такое преобразование должно совершаться явным образом, при этом все старшие биты, не умещающиеся в новом типе, просто отбрасываются - никакого округления или других действий для получения более корректного результата не производится.
+ __Расширение объектного типа (widening reference)__. Означает неявное восходящее приведение типов или переход от более конкретного типа к менее конкретному, т.е. переход от потомка к предку. Разрешено всегда и происходит автоматически.
+ __Сужение объектного типа (narrowing reference)__. Означает нисходящее приведение, то есть приведение от предка к потомку (подтипу). Возможно только если исходная переменная является подтипом приводимого типа. При несоответствии типов в момент выполнения выбрасывается исключение `ClassCastException`. Требует явного указания типа.
+ __Преобразование к строке (to String)__. Любой тип может быть приведен к строке, т.е. к экземпляру класса `String`.
+ __Запрещенные преобразования (forbidden)__. Не все приведения между произвольными типами допустимы. Например, к запрещенным преобразованиям относятся приведения от любого ссылочного типа к примитивному и наоборот (кроме преобразования к строке). Кроме того, невозможно привести друг к другу классы, находящиеся на разных ветвях дерева наследования и т.п.

При приведении ссылочных типов с самим объектом ничего не происходит, - меняется лишь тип ссылки, через которую происходит обращение к объекту.

Для проверки возможности приведения нужно воспользоваться оператором `instanceof`:

```java
Parent parent = new Child();
if (parent instanceof Child) {
    Child child = (Child) parent;
}
```

[to the top](#java-core)

## Когда в приложении может быть выброшено исключение `ClassCastException`?
`ClassCastException` (потомок `RuntimeException`) - исключение, которое будет выброшено при ошибке приведения типа.

[to the top](#java-core)

## Что такое литералы?
__Литералы__ — это явно заданные значения в коде программы — константы определенного типа, которые находятся в коде в момент запуска.
```java
class Test {
   int a = 0b1101010110;
   public static void main(String[] args) {
       System.out.println("Hello world!");       
   }
}
```
В этом классе “Hello world!” — литерал.

Переменная `a` - тоже литерал.

Литералы бывают разных типов, которые определяются их назначением и способом написания. 

[to the top](#java-core)

## Что такое _autoboxing («автоупаковка»)_ в Java и каковы правила упаковки примитивных типов в классы-обертки?
__Автоупаковка__ - это механизм неявной инициализации объектов классов-оберток (`Byte`, `Short`, `Integer`, `Long`, `Float`, `Double`, `Character`, `Boolean`) значениями соответствующих им исходных примитивных типов (`byte`, `short`, `int`...), без явного использования конструктора класса. 

+ Автоупаковка происходит при прямом присваивании примитива классу-обертке (с помощью оператора `=`), либо при передаче примитива в параметры метода (типа класса-обертки). 

+ Автоупаковке в классы-обертки могут быть подвергнуты как переменные примитивных типов, так и константы времени компиляции (литералы и `final`-примитивы). При этом литералы должны быть синтаксически корректными для инициализации переменной исходного примитивного типа.

+ Автоупаковка переменных примитивных типов требует точного соответствия типа исходного примитива типу класса-обертки. Например, попытка упаковать переменную типа `byte` в `Short`, без предварительного явного приведения `byte` в `short` вызовет ошибку компиляции.

+ Автоупаковка констант примитивных типов допускает более широкие границы соответствия. В этом случае компилятор способен предварительно осуществлять неявное расширение/сужение типа примитивов:
    1) неявное расширение/сужение исходного типа примитива до типа примитива, соответствующего классу-обертке (для преобразования `int` в `Byte`, сначала компилятор самостоятельно неявно сужает `int` к `byte`)
    2) автоупаковку примитива в соответствующий класс-обертку. Однако, в этом случае существуют два дополнительных ограничения:
        a) присвоение примитива обертке может производится только оператором `=` (нельзя передать такой примитив в параметры метода без явного приведения типов)
        b) тип левого операнда не должен быть старше чем `Character`, тип правого не должен старше, чем `int`: допустимо расширение/сужение `byte` в/из `short`, `byte` в/из `char`, `short` в/из `char` и только сужение `byte` из `int`, `short` из `int`, `char` из `int`. Все остальные варианты требуют явного приведения типов).

Дополнительной особенностью целочисленных классов-оберток, созданных автоупаковкой констант в диапазоне `-128 ... +127` является то, что они кэшируются JVM. Поэтому такие обертки с одинаковыми значениями будут являться ссылками на один объект.

[to the top](#java-core)

## Какие есть особенности класса `String`?
+ Это неизменяемый (immutable) и финализированный тип данных;
+ Все объекты класса `String` JVM хранит в пуле строк;
+ Объект класса `String` можно получить, используя двойные кавычки;
+ Можно использовать оператор `+` для конкатенации строк;
+ Начиная с Java 7 строки можно использовать в конструкции `switch`.

[to the top](#java-core)

## Почему `String` неизменяемый и финализированный класс?
Есть несколько преимуществ в неизменности строк:

+ Пул строк возможен только потому, что строка неизменяемая, таким образом виртуальная машина сохраняет больше свободного места в _Heap_, поскольку разные строковые переменные указывают на одну и ту же переменную в пуле. Если бы строка была изменяемой, то интернирование строк не было бы возможным, потому что изменение значения одной переменной отразилось бы также и на остальных переменных, ссылающихся на эту строку.
+ Если строка будет изменяемой, тогда это станет серьезной угрозой безопасности приложения. Например, имя пользователя базы данных и пароль передаются строкой для получения соединения с базой данных и в программировании сокетов реквизиты хоста и порта передаются строкой. Так как строка неизменяемая, её значение не может быть изменено, в противном случае злоумышленник может изменить значение ссылки и вызвать проблемы в безопасности приложения.
+ Неизменяемость позволяет избежать синхронизации: строки безопасны для многопоточности и один экземпляр строки может быть совместно использован различными потоками.
+ Строки используются _classloader_ и неизменность обеспечивает правильность загрузки класса.
+ Поскольку строка неизменяемая, её `hashCode()` кэшируется в момент создания и нет необходимости рассчитывать его снова. Это делает строку отличным кандидатом для ключа в `HashMap` т.к. его обработка происходит быстрее.

[to the top](#java-core)

## Почему `char[]` предпочтительнее `String` для хранения пароля?
С момента создания строка остаётся в пуле, до тех пор, пока не будет удалена сборщиком мусора. Поэтому, даже после окончания использования пароля, он некоторое время продолжает оставаться доступным в памяти и способа избежать этого не существует. Это представляет определённый риск для безопасности, поскольку кто-либо, имеющий доступ к памяти сможет найти пароль в виде текста.
В случае использования массива символов для хранения пароля имеется возможность очистить его сразу по окончанию работы с паролем, позволяя избежать риска безопасности, свойственного строке.

[to the top](#java-core)

## Почему строка является популярным ключом в `HashMap` в Java?
Поскольку строки неизменяемы, их хэш код вычисляется и кэшируется в момент создания, не требуя повторного пересчета при дальнейшем использовании. Поэтому в качестве ключа `HashMap` они будут обрабатываться быстрее.

[to the top](#java-core)

## Что делает метод `intern()` в классе `String`?.
Метод `intern()` используется для сохранения строки в пуле строк или получения ссылки, если такая строка уже находится в пуле.

[to the top](#java-core)

## Можно ли использовать строки в конструкции `switch`?
Да, начиная с Java 7 в операторе `switch` можно использовать строки, ранние версии Java не поддерживают этого. При этом:

+ участвующие строки чувствительны к регистру;
+ используется метод `equals()` для сравнения полученного значения со значениями `case`, поэтому во избежание `NullPointerException` стоит предусмотреть проверку на `null`.
+ согласно документации, Java 7 для строк в `switch`, компилятор Java формирует более эффективный байткод для строк в конструкции `switch`, чем для сцепленных условий `if`-`else`.

[to the top](#java-core)

## What is the difference between `String`, `StringBuffer`, `StringBuilder`?
Class `String` is _immutable_ you can't modify instance of this class, it is possible only to replace it with a new one.

Class `StringBuffer` is mutable - you should use `StringBuffer` when you often need to modify your string. 

Class `StringBuilder` was added in Java 5 it's identical to `StringBuffer` except that it is not synchronized and
therefore its methods are executed much faster.

[to the top](#java-core)


## What do you know about `Object` class? What are the methods in it?
`Object` is a parent class for all other objects in Java. Any class is inherited from `Object` and inherits his methods:

`public boolean equals(Object obj)` – to compare objects.

`int hashCode()` – returns hash code for the object;

`String toString()` – returns string representation of an object;

`Class getClass()` – returns object's class during runtime;

`protected Object clone()` – creates and returns copy of an object;

`void notify()` – wakes up a single thread that is waiting on this object's monitor

`void notifyAll()` – wakes up all threads that are waiting on this object's monitor

`void wait()` – Causes the current thread to wait until another thread invokes the `notify()` method or the `notifyAll()` method for this object;

`void wait(long timeout)` – Causes the current thread to wait until either another thread invokes the `notify()` method or the `notifyAll()` method for this object,
or a specified amount of time has elapsed.

`void wait(long timeout, int nanos)` – Causes the current thread to wait until another thread invokes the `notify()` method or the `notifyAll()` method for this object, 
or some other thread interrupts the current thread, or a certain amount of real time has elapsed;

`protected void finalize()` – Called by the garbage collector on an object when garbage collection determines that there are no more references to the object

[to the top](#java-core)

## Is an array an object in Java?
An array in java is an object.
In java language, arrays are objects which are dynamically created.

[JavaDoc](https://docs.oracle.com/javase/specs/jls/se8/html/jls-4.html#jls-4.3.1)
[GeeksForGeeks](https://www.geeksforgeeks.org/array-primitive-type-object-java/)

## Дайте определение понятию «конструктор».
__Конструктор__ — это специальный метод, у которого отсутствует возвращаемый тип и который имеет то же имя, что и класс, в котором он используется. Конструктор вызывается при создании нового объекта класса и определяет действия необходимые для его инициализации.

[to the top](#java-core)

## What is default constructor?
A **default constructor** is a constructor created by the compiler if we do not define any constructor(s) for a class. It doesn't take any
parameters

```java
public ClassName() {}
```

If a class already has a constructor defined, then the default constructor will not be created and, if necessary, it must be described explicitly.

[to the top](#java-core)

## Чем отличаются конструктор по-умолчанию, конструктор копирования и конструктор с параметрами?

У конструктора по умолчанию отсутствуют какие-либо аргументы. Конструктор копирования принимает в качестве аргумента уже существующий объект класса для последующего создания его клона. Конструктор с параметрами имеет в своей сигнатуре аргументы (обычно необходимые для инициализации полей класса).

[to the top](#java-core)

## Где и как вы можете использовать приватный конструктор?
Приватный (помеченный ключевым словом `private`, скрытый) конструктор может использоваться публичным статическим методом генерации объектов данного класса. Также доступ к нему разрешён вложенным классам и может использоваться для их нужд.

[to the top](#java-core)

## Расскажите про классы-загрузчики и про динамическую загрузку классов.
Основа работы с классами в Java — классы-загрузчики, обычные Java-объекты, предоставляющие интерфейс для поиска и создания объекта класса по его имени во время работы приложения.

В начале работы программы создается 3 основных загрузчика классов:

+ __базовый загрузчик (bootstrap/primordial)__. Загружает основные системные и внутренние классы JDK (_Core API_ - пакеты `java.*` (`rt.jar` и `i18n.jar`) . Важно заметить, что базовый загрузчик является _«Изначальным»_ или _«Корневым»_ и частью JVM, вследствие чего его нельзя создать внутри кода программы.
+ __загрузчик расширений (extention)__. Загружает различные пакеты расширений, которые располагаются в директории `<JAVA_HOME>/lib/ext` или другой директории, описанной в системном параметре `java.ext.dirs`. Это позволяет обновлять и добавлять новые расширения без необходимости модифицировать настройки используемых приложений. Загрузчик расширений реализован классом `sun.misc.Launcher$ExtClassLoader`. 
+ __системный загрузчик (system/application)__. Загружает классы, пути к которым указаны в переменной окружения `CLASSPATH` или пути, которые указаны в командной строке запуска JVM после ключей `-classpath` или `-cp`. Системный загрузчик реализован классом `sun.misc.Launcher$AppClassLoader`.

Загрузчики классов являются иерархическими: каждый из них (кроме базового) имеет родительский загрузчик и в большинстве случаев, перед тем как попробовать загрузить класс самостоятельно, он посылает вначале запрос родительскому загрузчику загрузить указанный класс. Такое делегирование позволяет загружать классы тем загрузчиком, который находится ближе всего к базовому в иерархии делегирования. Как следствие поиск классов будет происходить в источниках в порядке их доверия: сначала в библиотеке _Core API_, потом в папке расширений, потом в локальных файлах `CLASSPATH`. 

Процесс загрузки класса состоит из трех частей:

+ _Loading_ – на этой фазе происходит поиск и физическая загрузка файла класса в определенном источнике (в зависимости от загрузчика). Этот процесс определяет базовое представление класса в памяти. На этом этапе такие понятия как «методы», «поля» и т.д. пока не известны.
+ _Linking_ – процесс, который может быть разбит на 3 части:
    + _Bytecode verification_ – проверка байт-кода на соответствие требованиям, определенным в спецификации JVM.
    + _Class preparation_ – создание и инициализация необходимых структур, используемых для представления полей, методов, реализованных интерфейсов и т.п., определенных в загружаемом классе.
    + _Resolving_ – загрузка набора классов, на которые ссылается загружаемый класс.
+ _Initialization_ – вызов статических блоков инициализации и присваивание полям класса значений по умолчанию.

Динамическая загрузка классов в Java имеет ряд особенностей:

+ _отложенная (lazy) загрузка и связывание классов_. Загрузка классов производится только при необходимости, что позволяет экономить ресурсы и распределять нагрузку.
+ _проверка корректности загружаемого кода (type safeness)_. Все действия связанные с контролем использования типов производятся только во время загрузки класса, позволяя избежать дополнительной нагрузки во время выполнения кода.
+ _программируемая загрузка_. Пользовательский загрузчик полностью контролирует процесс получения запрошенного класса — самому ли искать байт-код и создавать класс или делегировать создание другому загрузчику. Дополнительно существует возможность выставлять различные атрибуты безопасности для загружаемых классов, позволяя таким образом работать с кодом из ненадежных источников.
+ _множественные пространства имен_. Каждый загрузчик имеет своё пространство имён для создаваемых классов. Соответственно, классы, загруженные двумя различными загрузчиками на основе общего байт-кода, в системе будут различаться.

Существует несколько способов инициировать загрузку требуемого класса:

+ явный: вызов `ClassLoader.loadClass()` или `Class.forName()` (по умолчанию используется загрузчик, создавший текущий класс, но есть возможность и явного указания загрузчика);
+ неявный: когда для дальнейшей работы приложения требуется ранее не использованный класс, JVM инициирует его загрузку.

[to the top](#java-core)

## Что такое _Reflection_?
__Рефлексия (Reflection)__ - это механизм получения данных о программе во время её выполнения (runtime). В Java _Reflection_ осуществляется с помощью _Java Reflection API_, состоящего из классов пакетов `java.lang` и `java.lang.reflect`.

Возможности Java Reflection API: 

+ Определение класса объекта;
+ Получение информации о модификаторах класса, полях, методах, конструкторах и суперклассах;
+ Определение интерфейсов, реализуемых классом;
+ Создание экземпляра класса;
+ Получение и установка значений полей объекта;
+ Вызов методов объекта;
+ Создание нового массива.

[to the top](#java-core)

## Why is `equals()` needed? How does it differ from the `==` operation?
Method `equals()` indicates whether some other object is "equal to" this one

When we compare objects using only using `==` sign the comparison takes place only between links. 
When we compare using overridden `equals()` we compare objects by their internal state

[to the top](#java-core)

## Если вы хотите переопределить `equals()`, какие условия должны выполняться?
## Какими свойствами обладает порождаемое `equals()` отношение эквивалентности?
+ _Рефлексивность_: для любой ссылки на значение `x`, `x.equals(x)` вернет `true`;
+ _Симметричность_: для любых ссылок на значения `x` и `y`, `x.equals(y)` должно вернуть `true`, тогда и только тогда, когда `y.equals(x)` возвращает `true`.
+ _Транзитивность_: для любых ссылок на значения `x`, `y` и `z`, если `x.equals(y)` и `y.equals(z)` возвращают `true`, тогда и `x.equals(z)` вернёт `true`;
+ _Непротиворечивость_: для любых ссылок на значения `х` и `у`, если несколько раз вызвать `х.equals(y)`, постоянно будет возвращаться значение `true` либо постоянно будет возвращаться значение `false` при условии, что никакая информация, используемая при сравнении объектов, не поменялась.

Для любой ненулевой ссылки на значение `х` выражение `х.equals(null)` должно возвращать `false`.

[to the top](#java-core)

## Правила переопределения метода `Object.equals()`.
1. Использование оператора `==` для проверки, является ли аргумент ссылкой на указанный объект. Если является, возвращается `true`. Если сравниваемый объект `== null`, должно вернуться `false`.
2. Использование вызова метода `getClass()` для проверки, имеет ли аргумент правильный тип. Если не имеет, возвращается `false`.
3. Приведение аргумента к правильному типу. Поскольку эта операция следует за проверкой `instanceof` она гарантированно будет выполнена.
4. Обход всех значимых полей класса и проверка того, что значение поля в текущем объекте и значение того же поля в проверяемом на эквивалентность аргументе соответствуют друг другу. Если проверки для всех полей прошли успешно, возвращается результат `true`, в противном случае - `false`.

По окончанию переопределения метода `equals()` следует проверить: является ли порождаемое отношение эквивалентности рефлексивным, симметричным, транзитивным и непротиворечивым? Если ответ отрицательный, метод подлежит соответствующей правке.

[to the top](#java-core)

## What if we compare using `==` two `boolean` values `new Boolean(false)` and `Boolean.FALSE`?

In this case we will get `false` result because we create `Boolean` wrapper object using `new` keyword 
and compare it with static instance of `Boolean`, but we compare them not by using `equals()`, but by 
references, and they will have different references because we are comparing different objects.

[to the top](#java-core)

## What if we compare using `==` two `Integer` values?
When we compare `Interger` values which are created like this: `Integer int1 = value`, 
result of comparison will depend on init value of both variables, if their values are in range `-128..127`
(highest value may be configured by property) then it's value returned from cache and comparison of the
same `Integer` objects from cache by value return `true`

If our value is out of cached range, but also created like `Integer int1 = value`, we will compare different 
objects and result of this comparison will be `false`

But any time you compare objects which are created explicitly using Integer's constructor like 
`Integer int2 = new Integer(anyIntValue)` and compare such objects you will get `false` result, because 
you'll have 2 separate objects in heap(even if they both contain the same value)

The same applies for all java wrapper classes and their reference comparisons, for `Character` it's range for 
chars between unicodes: `0..127` 

[Source code to see how caching works](https://github.com/openjdk/jdk/blob/master/src/java.base/share/classes/java/lang/Integer.java#L977)

## What happens when we compare `int` and `Integer` value using `==`?
When we compare primitive type with its wrapper type, then Wrapper object will be unboxed to primitive type
and if their values are the same, we will get `true` as result of comparing them using `==`  

[Docs](https://docs.oracle.com/javase/specs/jls/se8/html/jls-5.html#jls-5.1.7)

## Какая связь между `hashCode()` и `equals()`?
## Если `equals()` переопределен, есть ли какие-либо другие методы, которые следует переопределить?
Равные объекты должны возвращать одинаковые хэш коды. При переопределении `equals()` нужно обязательно переопределять и метод `hashCode()`.

[to the top](#java-core)

## Что будет, если переопределить `equals()` не переопределяя `hashCode()`? Какие могут возникнуть проблемы?
Классы и методы, которые используют правила этого контракта могут работать некорректно. Так для `HashMap` это может привести к тому, что пара «ключ-значение», которая была в неё помещена при использовании нового экземпляра ключа не будет в ней найдена.

[to the top](#java-core)

## Каким образом реализованы методы `hashCode()` и `equals()` в классе `Object`?
Реализация метода `Object.equals()` сводится к проверке на равенство двух ссылок:

```java
public boolean equals(Object obj) {
  return (this == obj);
}
```

Реализация метода `Object.hashCode()` описана как `native`, т.е. определенной не с помощью Java кода и обычно возвращает адрес объекта в памяти:

```java 
public native int hashCode();
```

[to the top](#java-core)

## What compares will return `true`?
```java
    public static void main(String[] args) {
        String s1 = "hello";
        final String s2 = "hel";
        String s3 = "lo";
        String s4 = "hello";

        System.out.println(s1 == s4); // #1
        System.out.println(s1 == s2 + s3); // #2
        System.out.println(s1 == s2 + "lo"); // #3
    }
```
First comparison will print `true` because literals are interned by
the compiler and thus refer to the same object

Second comparison will print `false` because `s3` string value isn't final and because of that 
compiler don't know what value will be after concatenating s2 and s3 strings, this value is only
might be calculated in runtime, and it won't be added to the string pool.

Third comparison will also print `true` because compiler knows all values of `s1 == s2 + "lo"` 
expression and it interns `s2 + "lo"` value to the string pool. Because we already have `"hello"`
value in our string pool both of comparing references will reference the same object, so as 
we comparing only references(because we use `==` sing) we will get `true` as the result

[to the top](#java-core)

## Для чего нужен метод `hashCode()`?
Метод `hashCode()` необходим для вычисления хэш кода переданного в качестве входного параметра объекта. В Java это целое число, в более широком смысле - битовая строка фиксированной длины, полученная из массива произвольной длины. Этот метод реализован таким образом, что для одного и того же входного объекта, хэш код всегда будет одинаковым. Следует понимать, что в Java множество возможных хэш кодов ограничено типом `int`, а множество объектов ничем не ограничено. Из-за этого, вполне возможна ситуация, что хэш коды разных объектов могут совпасть:

+ если хэш коды разные, то и объекты гарантированно разные;
+ если хэш коды равны, то объекты не обязательно равны(могут быть разные).

[to the top](#java-core)

## Каковы правила переопределения метода `Object.hashCode()`?
## Есть ли какие-либо рекомендации о том, какие поля следует использовать при подсчете `hashCode()`?
Общий совет: выбирать поля, которые с большой долью вероятности будут различаться. Для этого необходимо использовать уникальные, лучше всего примитивные поля, например, такие как `id`, `uuid`. При этом нужно следовать правилу, если поля задействованы при вычислении `hashCode()`, то они должны быть задействованы и при выполнении `equals()`.

[to the top](#java-core)

## Могут ли у разных объектов быть одинаковые `hashCode()`?
Да, могут. Метод `hashCode()` не гарантирует уникальность возвращаемого значения. Ситуация, когда у разных объектов одинаковые хэш коды называется _коллизией_. Вероятность возникновения коллизии зависит от используемого алгоритма генерации хэш кода.

[to the top](#java-core)

## Если у класса `Point{int x, y;}` реализовать метод `equals(Object that) {(return this.x == that.x && this.y == that.y)}`, но сделать хэш код в виде `int hashCode() {return x;}`, то будут ли корректно такие точки помещаться и извлекаться из `HashSet`?
`HashSet` использует `HashMap` для хранения элементов. При добавлении элемента в `HashMap` вычисляется хэш код, по которому определяется позиция в массиве, куда будет вставлен новый элемент. У всех экземпляров класса `Point` хэш код будет одинаковым для всех объектов с одинаковым `x`, что приведёт к вырождению хэш таблицы в список. 

При возникновении коллизии в `HashMap` осуществляется проверка на наличие элемента в списке: `e.hash == hash && ((k = e.key) == key || key.equals(k))`. Если элемент найден, то его значение перезаписывается. В нашем случае для разных объектов метод `equals()` будет возвращать `false`. Соответственно новый элемент будет успешно добавлен в `HashSet`. Извлечение элемента также будет осуществляться успешно. Но производительность такого кода будет невысокой и преимущества хэш таблиц использоваться не будут.

[to the top](#java-core)

## Могут ли у разных объектов `(ref0 != ref1)` быть `ref0.equals(ref1) == true`?
Да, могут. Для этого в классе этих объектов должен быть переопределен метод `equals()`.

Если используется метод `Object.equals()`, то для двух ссылок `x` и `y` метод вернет `true` тогда и только тогда, когда обе ссылки указывают на один и тот же объект (т.е. `x == y` возвращает `true`).

[to the top](#java-core)

## Могут ли у разных ссылок на один объект `(ref0 == ref1)` быть `ref0.equals(ref1) == false`?
В общем случае - могут, если метод `equals()` реализован некорректно и не выполняет свойство рефлексивности: для любых ненулевых ссылок `x` метод `x.equals(x)` должен возвращать `true`.

[to the top](#java-core)

## Можно ли так реализовать метод `equals(Object that) {return this.hashCode() == that.hashCode()}`?
Строго говоря нельзя, поскольку метод `hashCode()` не гарантирует уникальность значения для каждого объекта. Однако для сравнения экземпляров класса `Object` такой код допустим, т.к. метод `hashCode()` в классе `Object` возвращает уникальные значения для разных объектов (его вычисление основано на использовании адреса объекта в памяти).

[to the top](#java-core)

## В `equals()` требуется проверять, что аргумент `equals(Object that)` такого же типа что и сам объект. В чем разница между `this.getClass() == that.getClass()` и `that instanceof MyClass`?
Оператор `instanceof` сравнивает объект и указанный тип. Его можно использовать для проверки является ли данный объект экземпляром некоторого класса, либо экземпляром его дочернего класса, либо экземпляром класса, который реализует указанный интерфейс.

`this.getClass() == that.getClass()` проверяет два класса на идентичность, поэтому для корректной реализации контракта метода `equals()` необходимо использовать точное сравнение с помощью метода `getClass()`.

[to the top](#java-core)

## Можно ли реализовать метод `equals()` класса `MyClass` вот так: `class MyClass {public boolean equals(MyClass that) {return this == that;}}`?
Реализовать можно, но данный метод не переопределяет метод `equals()` класса `Object`, а перегружает его.

[to the top](#java-core)

## Есть класс `Point{int x, y;}`. Почему хэш код в виде `31 * x + y` предпочтительнее чем `x + y`?
Множитель создает зависимость значения хэш кода от очередности обработки полей, что в итоге порождает лучшую хэш функцию.

[to the top](#java-core)

## Расскажите про интерфейс `Comparable<T>`, чем он отличается от интерфейса `Comparator<T>`?
Интерфейс `Comparable<T>` - это функциональный интерфейс с абстрактным методом `compareTo()`, данный метод определяет
естественный порядок(_natural order_) расположения элементов данного класса при сортировке. 
При переопределении данного метода, возвращаемое им значение должно быть согласовано с возвращаемым значением метода 
`equals()` данного класса. 

Интерфейс `Comparator<T>` - интерфейс, который определяет порядок сортировки объектов, используя переопределённый метод 
`compare()`, его имплементирует уже не сам класс, объекты которого мы собираемся сортировать, а какой-то другой класс. 
Данный интерфейс используется, если у нашего класса уже переопределен метод `compareTo()` и нам нужно задать какой-либо 
другой порядок сортировки наших объектах, тогда мы можем передать `Comparator<T>` в методы, подобные `Collections.sort()` 
и `Arrays.sort()`. Возращаемое значение метода `compare()` также должно быть согласовано с методом `equals()`

- Нужно использовать `Comparable<T>` когда мы хотим определить _natural ordering_ для экземпляров нашего класса, как правило,
естественным порядком является самый часто встречающийся порядок расположения наших объектов.
- Используя `Comarable<T>` мы можем определить только один порядок сортировки наших объектов, а передавая в метод 
`Collections.sort()` различные реализации `Comapator<T>` можем определять разную логику сортировки объектов.


[Comparable документация](https://docs.oracle.com/javase/8/docs/api/java/lang/Comparable.html)

[Compartor документация](https://docs.oracle.com/javase/8/docs/api/java/util/Comparator.html)

[to the top](#java-core)

## Почему при реализации методов `compareTo()` и `compare()` интерфейсов `Comparable<T>` и `Comparator<T>` соответственно, необходимо их согласование с `equals()`?
Порядок объектов в коллекции, который определяется `Comparable<T>` и `Comparator<T>` крайне рекомендуется(хотя и необязательно)
согласовывать с `equals()`, если этого не сделать, то поведение объектов в некоторых коллекциях имплементирующих интерфейсы
`SortedMap<K, V>` и `SortedSet<E>` будет непредсказуемым. 
Если мы планируем добавлять сравниваемые объекты в одну из таких коллекций, 
то необходимо соблюсти условие:
если `obj1.compareTo(obj2) == 0` тогда `obj1.equals(obj2) == true`, с одним исключением, что `obj1.compareTo(null)` должно
выбрасывать `NullPointerException` несмотря на то, что `obj1.equals(null) == false`  

Например, мы добавляем 2 ключа a и b таких, что `(!a.equals(b) && a.compareTo(b) == 0)` в `TreeSet`. Вторая операция добавления 
элемента не добавит его в `TreeSet`, потому что с точки зрения `TreeSet` эти элементы равны. Из-за такой несогласованности
мы можем получить странное поведение объектов в таких коллекциях:
```java
> BigDecimal z = new BigDecimal("0.0")
> BigDecimal zz = new BigDecimal("0.00")
> z.compareTo(zz)
0
> z.equals(zz)
false
> TreeSet<BigDecimal> ts = new TreeSet<>()
> ts.add(z)
> ts.contains(z)
true
> z.equals(ts.iterator().next())
true
> ts.contains(zz)
true
> zz.equals(ts.iterator().next())
false
```
Все стандартные классы в java, имплементирующие `Comparable<T>` имеют согласованный с `compareTo()` метод `equals()`, 
за исключением класса `BigDecimal`.

Аналогичное условие должно соблюдаться и для метода `compare()` `c.compare(e1, e2) == 0` => `e1.equals(e2) == true`

[Comparable документация](https://docs.oracle.com/javase/8/docs/api/java/lang/Comparable.html)

[Compartor документация](https://docs.oracle.com/javase/8/docs/api/java/util/Comparator.html)

[Stack overflow question](https://stackoverflow.com/a/53901802/21479048)

[to the top](#java-core)
## Расскажите про клонирование объектов.
Использование оператора присваивания не создает нового объекта, а лишь копирует ссылку на объект. Таким образом, две ссылки указывают на одну и ту же область памяти, на один и тот же объект. Для создания нового объекта с таким же состоянием используется клонирование объекта. 

Класс `Object` содержит `protected` метод `clone()`, осуществляющий побитовое копирование объекта производного класса. Однако сначала необходимо переопределить метод `clone()` как `public` для обеспечения возможности его вызова. В переопределенном методе следует вызвать базовую версию метода `super.clone()`, которая и выполняет собственно клонирование. 

Чтобы окончательно сделать объект клонируемым, класс должен реализовать интерфейс `Cloneable`. Интерфейс `Cloneable` не содержит методов относится к маркерным интерфейсам, а его реализация гарантирует, что метод `clone()` класса `Object` возвратит точную копию вызвавшего его объекта с воспроизведением значений всех его полей. В противном случае метод генерирует исключение `CloneNotSupportedException`. Следует отметить, что при использовании этого механизма объект создается без вызова конструктора.

Это решение эффективно только в случае, если поля клонируемого объекта представляют собой значения базовых типов и их обёрток или неизменяемых (immutable) объектных типов. Если же поле клонируемого типа является изменяемым ссылочным типом, то для корректного клонирования требуется другой подход. Причина заключается в том, что при создании копии поля оригинал и копия представляют собой ссылку на один и тот же объект. В этой ситуации следует также клонировать и сам объект поля класса.

Такое клонирование возможно только в случае, если тип атрибута класса также реализует интерфейс `Cloneable` и переопределяет метод `clone()`. Так как, если это будет иначе вызов метода невозможен из-за его недоступности. Отсюда следует, что если класс имеет суперкласс, то для реализации механизма клонирования текущего класса-потомка необходимо наличие корректной реализации такого механизма в суперклассе. При этом следует отказаться от использования объявлений `final` для полей объектных типов по причине невозможности изменения их значений при реализации клонирования.

Помимо встроенного механизма клонирования в Java для клонирования объекта можно использовать:

+ __Специализированный конструктор копирования__ - в классе описывается конструктор, который принимает объект этого же класса и инициализирует поля создаваемого объекта значениями полей переданного.
+ __Фабричный метод__ - (Factory method), который представляет собой статический метод, возвращающий экземпляр своего класса.
+ __Механизм сериализации__ - сохранение и последующее восстановление объекта в/из потока байтов.

[to the top](#java-core)

## В чем отличие между _поверхностным_ и _глубоким_ клонированием?
__Поверхностное копирование__ копирует настолько малую часть информации об объекте, насколько это возможно. По умолчанию, клонирование в Java является поверхностным, т.е. класс `Object` не знает о структуре класса, которого он копирует. Клонирование такого типа осуществляется JVM по следующим правилам: 

+ Если класс имеет только члены примитивных типов, то будет создана совершенно новая копия объекта и возвращена ссылка на этот объект.
+ Если класс помимо членов примитивных типов содержит члены ссылочных типов, то тогда копируются ссылки на объекты этих классов. Следовательно, оба объекта будут иметь одинаковые ссылки.

__Глубокое копирование__ дублирует абсолютно всю информацию объекта:
+ Нет необходимости копировать отдельно примитивные данные;
+ Все члены ссылочного типа в оригинальном классе должны поддерживать клонирование. Для каждого такого члена при переопределении метода `clone()` должен вызываться `super.clone()`;
+ Если какой-либо член класса не поддерживает клонирование, то в методе клонирования необходимо создать новый экземпляр этого класса и скопировать каждый его член со всеми атрибутами в новый объект класса, по одному.

[to the top](#java-core)

## Какой способ клонирования предпочтительней?
Наиболее безопасным и, следовательно, предпочтительным способом клонирования является использование специализированного конструктора копирования: 

+ Отсутствие ошибок наследования (не нужно беспокоиться, что у наследников появятся новые поля, которые не будут склонированы через метод `clone()`);
+ Поля для клонирования указываются явно;
+ Возможность клонировать даже `final` поля.

[to the top](#java-core)

## Почему метод `clone()` объявлен в классе `Object`, а не в интерфейсе `Cloneable`?
Метод `clone()` объявлен в классе `Object` с указанием модификатора `native`, чтобы обеспечить доступ к стандартному механизму поверхностного копирования объектов. Одновременно он объявлен и как `protected`, чтобы нельзя было вызвать этот метод у не переопределивших его объектов. Непосредственно интерфейс `Cloneable` является маркерным (не содержит объявлений методов) и нужен только для обозначения самого факта, что данный объект готов к тому, чтобы быть клонированным. Вызов переопределённого метода `clone()` у не `Cloneable` объекта вызовет выбрасывание `CloneNotSupportedException`.

[to the top](#java-core)

## Опишите иерархию исключений.
Исключения делятся на несколько классов, но все они имеют общего предка — класс `Throwable`, потомками которого являются классы `Exception` и `Error`.

__Ошибки (Errors)__ представляют собой более серьёзные проблемы, которые, согласно спецификации Java, не следует обрабатывать в собственной программе, поскольку они связаны с проблемами уровня JVM. Например, исключения такого рода возникают, если закончилась память доступная виртуальной машине.

__Исключения (Exceptions)__ являются результатом проблем в программе, которые в принципе решаемы, предсказуемы и последствия которых возможно устранить внутри программы. Например, произошло деление целого числа на ноль.

[to the top](#java-core)

## What types of exceptions do you know?
## Что такое _checked_ и _unchecked exception_?
В Java все исключения делятся на два типа:

+ __checked (контролируемые/проверяемые исключения)__ должны обрабатываться блоком `catch` или описываться в заголовке метода (например, `throws IOException`). Наличие такого обработчика/модификатора в заголовке метода проверяется на этапе компиляции;
+ __unchecked (неконтролируемые/непроверяемые исключения)__, к которым относятся ошибки `Error` (например, `OutOfMemoryError`), обрабатывать которые не рекомендуется и исключения времени выполнения, представленные классом `RuntimeException` и его наследниками (например, `NullPointerException`), которые могут не обрабатываться блоком `catch` и не быть описанными в заголовке метода.

[to the top](#java-core)

## Какой оператор позволяет принудительно выбросить исключение?
Это оператор `throw`:

```java
throw new Exception();
```

[to the top](#java-core)

## О чем говорит ключевое слово `throws`?
Модификатор `throws` прописывается в заголовке метода и указывает на то, что метод потенциально может выбросить исключение с указанным типом.

[to the top](#java-core)

## Как написать собственное («пользовательское») исключение?
Необходимо унаследоваться от базового класса требуемого типа исключений (например, от `Exception` или `RuntimeException`).

```java
class CustomException extends Exception {
    public CustomException() {
        super();
    }

    public CustomException(final String string) {
        super(string + " is invalid");
    }

    public CustomException(final Throwable cause) {
        super(cause);
    }
}
```

[to the top](#java-core)

## Какие существуют _unchecked exception_?
Наиболее часто встречающиеся: `ArithmeticException`, `ClassCastException`, `ConcurrentModificationException`, `IllegalArgumentException`, `IllegalStateException`, `IndexOutOfBoundsException`, `NoSuchElementException`, `NullPointerException`, `UnsupportedOperationException`.

[to the top](#java-core)

## Что представляет из себя ошибки класса `Error`?
Ошибки класса `Error` представляют собой наиболее серьёзные проблемы уровня JVM. Например, исключения такого рода возникают, если закончилась память доступная виртуальной машине. Обрабатывать такие ошибки не запрещается, но делать этого не рекомендуется.

[to the top](#java-core)

## Что вы знаете о `OutOfMemoryError`?
`OutOfMemoryError` выбрасывается, когда виртуальная машина Java не может создать (разместить) объект из-за нехватки памяти, а сборщик мусора не может высвободить достаточное её количество.

Область памяти, занимаемая java процессом, состоит из нескольких частей. Тип `OutOfMemoryError` зависит от того, в какой из них не хватило места:

+ `java.lang.OutOfMemoryError: Java heap space`: Не хватает места в куче, а именно, в области памяти в которую помещаются объекты, создаваемые в приложении программно. Обычно проблема кроется в утечке памяти. Размер задается параметрами `-Xms` и `-Xmx`.
+ `java.lang.OutOfMemoryError: PermGen space`: (до версии Java 8) Данная ошибка возникает при нехватке места в _Permanent_ области, размер которой задается параметрами `-XX:PermSize` и `-XX:MaxPermSize`.
+ `java.lang.OutOfMemoryError: GC overhead limit exceeded`: Данная ошибка может возникнуть как при переполнении первой, так и второй областей. Связана она с тем, что памяти осталось мало и сборщик мусора постоянно работает, пытаясь высвободить немного места. Данную ошибку можно отключить с помощью параметра `-XX:-UseGCOverheadLimit`.
+ `java.lang.OutOfMemoryError: unable to create new native thread`: Выбрасывается, когда нет возможности создавать новые потоки.

[to the top](#java-core)

## Опишите работу блока _try-catch-finally_.
`try` — данное ключевое слово используется для отметки начала блока кода, который потенциально может привести к ошибке.
`catch` — ключевое слово для отметки начала блока кода, предназначенного для перехвата и обработки исключений в случае их возникновения.
`finally` — ключевое слово для отметки начала блока кода, который является дополнительным. Этот блок помещается после последнего блока `catch`. Управление передаётся в блок `finally` в любом случае, было выброшено исключение или нет.

Общий вид конструкции для обработки исключительной ситуации выглядит следующим образом:

```java
try { 
    //код, который потенциально может привести к исключительной ситуации 
} 
catch(SomeException e ) { //в скобках указывается класс конкретной ожидаемой ошибки  
    //код обработки исключительной ситуации
} 
finally {
    //необязательный блок, код которого выполняется в любом случае
}
```

[to the top](#java-core)

## Что такое механизм _try-with-resources_?
Данная конструкция, которая появилась в Java 7, позволяет использовать блок _try-catch_ не заботясь о закрытии ресурсов, используемых в данном сегменте кода.
Ресурсы объявляются в скобках сразу после `try`, а компилятор уже сам неявно создаёт секцию `finally`, в которой и происходит освобождение занятых в блоке ресурсов. Под ресурсами подразумеваются сущности, реализующие интерфейс `java.lang.Autocloseable`. 

Общий вид конструкции:

```java
try(/*объявление ресурсов*/) {
    //...
} catch(Exception ex) {
    //...
} finally {
    //...
}
```

Стоит заметить, что блоки `catch` и явный `finally` выполняются уже после того, как закрываются ресурсы в неявном `finally`.

[to the top](#java-core)

## Возможно ли использование блока _try-finally_ (без `catch`)?
Такая запись допустима, но смысла в такой записи не так много, всё же лучше иметь блок `catch`, в котором будет обрабатываться необходимое исключение.

[to the top](#java-core)

## Может ли один блок `catch` отлавливать сразу несколько исключений?
В Java 7 стала доступна новая языковая конструкция, с помощью которой можно перехватывать несколько исключений одним блоком `catch`:

```java
try {  
    //...
} catch(IOException | SQLException ex) {
    //...
}
```

[to the top](#java-core)

## Всегда ли исполняется блок `finally`?
Код в блоке `finally` будет выполнен всегда, независимо от того, выброшено исключение или нет.
Данный блок выполнится даже в том случае, если ошибка возникнет в блоке `catch`

[to the top](#java-core)

## Существуют ли ситуации, когда блок `finally` не будет выполнен?
Например, когда JVM «умирает» - в такой ситуации `finally` недостижим и не будет выполнен, так как происходит принудительный системный выход из программы:

```java
try { 
    System.exit(0); 
} catch(Exception e) { 
    e.printStackTrace(); 
} finally { }
```

[to the top](#java-core)

## Может ли метод _main()_ выбросить исключение во вне и если да, то где будет происходить обработка данного исключения?
Может и оно будет передано в виртуальную машину Java (JVM).

[to the top](#java-core)

## Предположим, есть метод, который может выбросить `IOException` и `FileNotFoundException` в какой последовательности должны идти блоки `catch`? Сколько блоков `catch` будет выполнено?
Общее правило: обрабатывать исключения нужно от «младшего» к старшему. Т.е. нельзя поставить в первый блок `catch(Exception ex) {}`, иначе все дальнейшие блоки `catch()` уже ничего не смогут обработать, т.к. любое исключение будет соответствовать обработчику `catch(Exception ex)`.

Таким образом, исходя из факта, что `FileNotFoundException extends IOException` сначала нужно обработать `FileNotFoundException`, а затем уже `IOException`:

```java
void method() {
    try {
        //...
    } catch (FileNotFoundException ex) {
        //...
    } catch (IOException ex) {
        //...
    }
}
```

[to the top](#java-core)   

## Is it allowed to return some value in `finally{}` or `catch{}` block?
Yes, you can do it, if you return value inside `catch{}` block, it will be normally returned if exception will 
be thrown inside `try{}` and `finally{}` isn't return some value.

In `finally{}` block you also can return some value, but this value will always overrride values which are returned 
in other blocks like `try{}` and `catch{}`, you should never return anything from `finally{}`, also you may disable 
the exception which is thrown in your method.

[to the top](#java-core)

## How do you think, are checked exceptions were bad design decision?

Usually, checked exceptions are meant for cases where you usually can recover from the exceptional situation.
Checked exceptions have pros and cons. 
Cons. 
- In some situations they may cause encapsulation violation if you method `throws SomeException` then some exceptions may 
cross module boundaries, which they shouldn't.
- Make code uglier and harder to read because of many `try{}catch{}` blocks.
- Novice programmer often will "swallow" exceptions simply wrap them in `RuntimeException` or by just leaving empty 
`catch{}` block

Pros
- Developer instantly notified that exceptional situation might happen and measures must have been taken
- Compile time safety for some situations

So, checked exceptions have more cons, but they are big part of java language and unlikely will be removed 
 

[to the top](#java-core)

## Что такое _generics_?
__Generics__ - это технический термин, обозначающий набор свойств языка позволяющих определять и использовать обобщенные типы и методы. 
Обобщенные типы или методы отличаются от обычных тем, что имеют типизированные параметры.

Примером использования обобщенных типов может служить _Java Collection Framework_. Так, класс `LinkedList<E>` - типичный обобщенный тип. Он содержит параметр `E`, который представляет тип элементов, которые будут храниться в коллекции. Создание объектов обобщенных типов происходит посредством замены параметризированных типов реальными типами данных. Вместо того, чтобы просто использовать `LinkedList`, ничего не говоря о типе элемента в списке, предлагается использовать точное указание типа `LinkedList<String>`, `LinkedList<Integer>` и т.п.

[to the top](#java-core)

## What is type erasure in java?
During the type erasure, the java complier erases all type parameters and replaces each with 
its first bound if the type parameter is bounded or `Object` if type parameter is unbounded.

When generics are _used_ they're converted into compile-time checks and execution-time casts.

## Why we can't use primitive type in generic code?
Because java use type-erased generics, so in runtime we don't have information about generic type, 
so any `T t` field is becoming `Object` type in runtime, but as primitives are not derived from `Object`, 
technically, they are not objects at all, they can't be erased to `Object` and can't be used in generics.

## What are pros and cons of java generics
Cons:
- Can't be used with primitives, like `List<byte>`
- Syntax for constraints can get confusing
- At execution time you can't tell type of object

Pros:
- Wildcarding allows covariance/contravariance to be specified at calling side, which is very neat in many situations

[stackoverflow](https://stackoverflow.com/a/520568)

## How code in example with generics will look after compilation?
```java
List<String> list = new ArrayList<String>();
list.add("Hi");
String x = list.get(0);
```

After compilation:
```java
List list = new ArrayList();
list.add("Hi");
String x = (String) list.get(0);
```

## Why java doesn't have reified generics?
In early versions of java, there is no generics, they were introduced only in Java 5, and they were 
implemented as type-erased generics, so information about type is only available in compile time, such 
decision were made because it allows backward compatibility with pre Java 5 code, because there is no information
about generics in runtime.

Java supports reification for most of the types, like primitives, non-parameterised types, array of primitives, etc.
But parameterized types (`List<Number>`) is not reifiable in Java and bounded parameterized 
types like `List<? extends Number>`, they lose their type information at runtime due type erasure. 

## What is heap pollution?
Heap pollution implies that we have bad data in our memory. In java language, heap pollution is a situation that occurs 
when a variable of parametrized type point to an object that is not of a that parametrized type. 

```java
class MyClass {
  public static void main(String[] args) {
    List<String> listOfStrings = new ArrayList<>();
    listOfStrings.add("Some string");
    
    List<Integer> listOfIntegers = (List<Integer>) (Object) listOfString;
    Integer firstElement = listOfIntegers.get(0);
    System.out.println(firstElement);
    
  }
}
```
This code will throw `ClassCastException` in runtime, and we get warning in compile time

[to the top](#java-core)


## Что такое _«интернационализация»_, _«локализация»_?
__Интернационализация (internationalization)__ - способ создания приложений, при котором их можно легко адаптировать для разных аудиторий, говорящих на разных языках.

__Локализация (localization)__ -  адаптация интерфейса приложения под несколько языков. Добавление нового языка может внести определенные сложности в локализацию интерфейса.

[to the top](#java-core)

# Источники
+ [Quizful](http://www.quizful.net/interview/java/)
+ [JavaStudy.ru](http://javastudy.ru/interview/java-oop2/)
+ [ggenikus.github.io](https://ggenikus.github.io/blog/2014/05/04/gc/)
+ [Санкт-Петербургская группа тестирования JVM](https://blogs.oracle.com/vmrobot/entry/основы_сборки_мусора_в_hotspot)
+ [Объектно-ориентированное программирование](http://oop-java.blogspot.ru/2006/02/blog-post_21.html)
+ [JavaRush](http://info.javarush.ru/)

[Вопросы для собеседования](README.md)

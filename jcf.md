[Вопросы для собеседования](README.md)

# Java Collections Framework
+ [Что такое _«коллекция»_?](#Что-такое-коллекция)
+ [Назовите основные интерфейсы JCF и их реализации.](#please-describe-main-interfaces-in-jcf-and-their-realizations)
+ [Расположите в виде иерархии следующие интерфейсы: `List`, `Set`, `Map`, `SortedSet`, `SortedMap`, `Collection`, `Iterable`, `Iterator`, `NavigableSet`, `NavigableMap`.](#Расположите-в-виде-иерархии-следующие-интерфейсы-list-set-map-sortedset-sortedmap-collection-iterable-iterator-navigableset-navigablemap)
+ [Почему `Map` — это не `Collection`, в то время как `List` и `Set` являются `Collection`?](#Почему-map--это-не-collection-в-то-время-как-list-и-set-являются-collection)
+ [В чем разница между классами `java.util.Collection` и `java.util.Collections`?](#В-чем-разница-между-классами-javautilcollection-и-javautilcollections)
+ [Что такое «fail-fast поведение»?](#Что-такое-fail-fast-поведение)
+ [Какая разница между fail-fast и fail-safe?](#Какая-разница-между-fail-fast-и-fail-safe)
+ [Приведите примеры итераторов, реализующих поведение fail-safe](#Приведите-примеры-итераторов-реализующих-поведение-fail-safe)
+ [Чем различаются `Enumeration` и `Iterator`.](#Чем-различаются-enumeration-и-iterator)
+ [Как между собой связаны `Iterable` и `Iterator`?](#Как-между-собой-связаны-iterable-и-iterator)
+ [Как между собой связаны `Iterable`, `Iterator` и «for-each»?](#Как-между-собой-связаны-iterable-iterator-и-for-each)
+ [Сравните `Iterator` и `ListIterator`.](#Сравните-iterator-и-listiterator)
+ [Что произойдет при вызове `Iterator.next()` без предварительного вызова `Iterator.hasNext()`?](#Что-произойдет-при-вызове-iteratornext-без-предварительного-вызова-iteratorhasnext)
+ [Сколько элементов будет пропущено, если `Iterator.next()` будет вызван после 10-ти вызовов `Iterator.hasNext()`?](#Сколько-элементов-будет-пропущено-если-iteratornext-будет-вызван-после-10-ти-вызовов-iteratorhasnext)
+ [Как поведёт себя коллекция, если вызвать `iterator.remove()`?](#Как-поведёт-себя-коллекция-если-вызвать-iteratorremove)
+ [Как поведёт себя уже инстанциированный итератор для `collection`, если вызвать `collection.remove()`?](#Как-поведёт-себя-уже-инстанциированный-итератор-для-collection-если-вызвать-collectionremove)
+ [Как избежать `ConcurrentModificationException` во время перебора коллекции?](#Как-избежать-concurrentmodificationexception-во-время-перебора-коллекции)
+ [Какая коллекция реализует дисциплину обслуживания FIFO?](#Какая-коллекция-реализует-дисциплину-обслуживания-fifo)
+ [Какая коллекция реализует дисциплину обслуживания FILO?](#Какая-коллекция-реализует-дисциплину-обслуживания-filo)
+ [Чем отличается `ArrayList` от `Vector`?](#Чем-отличается-arraylist-от-vector)
+ [Зачем добавили `ArrayList`, если уже был `Vector`?](#Зачем-добавили-arraylist-если-уже-был-vector)
+ [Чем отличается `ArrayList` от `LinkedList`? В каких случаях лучше использовать первый, а в каких второй?](#Чем-отличается-arraylist-от-linkedlist-В-каких-случаях-лучше-использовать-первый-а-в-каких-второй)
+ [Что работает быстрее `ArrayList` или `LinkedList`?](#Что-работает-быстрее-arraylist-или-linkedlist)
+ [Какое худшее время работы метода `contains()` для элемента, который есть в `LinkedList`?](#Какое-худшее-время-работы-метода-contains-для-элемента-который-есть-в-linkedlist)
+ [Какое худшее время работы метода `contains()` для элемента, который есть в `ArrayList`?](#Какое-худшее-время-работы-метода-contains-для-элемента-который-есть-в-arraylist)
+ [Какое худшее время работы метода `add()` для `LinkedList`?](#Какое-худшее-время-работы-метода-add-для-linkedlist)
+ [Какое худшее время работы метода `add()` для `ArrayList`?](#Какое-худшее-время-работы-метода-add-для-arraylist)
+ [Необходимо добавить 1 млн. элементов, какую структуру вы используете?](#Необходимо-добавить-1-млн-элементов-какую-структуру-вы-используете)
+ [Как происходит удаление элементов из `ArrayList`? Как меняется в этом случае размер `ArrayList`?](#Как-происходит-удаление-элементов-из-arraylist-Как-меняется-в-этом-случае-размер-arraylist)
+ [Предложите эффективный алгоритм удаления нескольких рядом стоящих элементов из середины списка, реализуемого `ArrayList`.](#Предложите-эффективный-алгоритм-удаления-нескольких-рядом-стоящих-элементов-из-середины-списка-реализуемого-arraylist)
+ [Сколько необходимо дополнительной памяти при вызове `ArrayList.add()`?](#Сколько-необходимо-дополнительной-памяти-при-вызове-arraylistadd)
+ [Сколько выделяется дополнительно памяти при вызове `LinkedList.add()`?](#Сколько-выделяется-дополнительно-памяти-при-вызове-linkedlistadd)
+ [Оцените количество памяти на хранение одного примитива типа `byte` в `LinkedList`?](#Оцените-количество-памяти-на-хранение-одного-примитива-типа-byte-в-linkedlist)
+ [Оцените количество памяти на хранение одного примитива типа `byte` в `ArrayList`?](#Оцените-количество-памяти-на-хранение-одного-примитива-типа-byte-в-arraylist)
+ [Для `ArrayList` или для `LinkedList` операция добавления элемента в середину (`list.add(list.size()/2, newElement)`) медленнее?](#Для-arraylist-или-для-linkedlist-операция-добавления-элемента-в-середину-listaddlistsize2-newelement-медленнее)
+ [В реализации класса `ArrayList` есть следующие поля: `Object[] elementData`, `int size`. Объясните, зачем хранить отдельно `size`, если всегда можно взять `elementData.length`?](#В-реализации-класса-arraylist-есть-следующие-поля-object-elementdata-int-size-Объясните-зачем-хранить-отдельно-size-если-всегда-можно-взять-elementdatalength)
+ [Сравните интерфейсы `Queue` и `Deque`.](#Сравните-интерфейсы-queue-и-deque)
+ [Кто кого расширяет: `Queue` расширяет `Deque`, или `Deque` расширяет `Queue`?](#Кто-кого-расширяет-queue-расширяет-deque-или-deque-расширяет-queue)
+ [Почему `LinkedList` реализует и `List`, и `Deque`?](#Почему-linkedlist-реализует-и-list-и-deque)
+ [`LinkedList` — это односвязный, двусвязный или четырехсвязный список?](#linkedlist--это-односвязный-двусвязный-или-четырехсвязный-список)
+ [Как перебрать элементы `LinkedList` в обратном порядке, не используя медленный `get(index)`?](#Как-перебрать-элементы-linkedlist-в-обратном-порядке-не-используя-медленный-getindex)
+ [Что позволяет сделать `PriorityQueue`?](#Что-позволяет-сделать-priorityqueue)
+ [`Stack` считается «устаревшим». Чем его рекомендуют заменять? Почему?](#stack-считается-устаревшим-Чем-его-рекомендуют-заменять-Почему)
+ [Зачем нужен `HashMap`, если есть `Hashtable`?](#Зачем-нужен-hashmap-если-есть-hashtable)
+ [В чем разница между `HashMap` и `IdentityHashMap`? Для чего нужна `IdentityHashMap`?](#В-чем-разница-между-hashmap-и-identityhashmap-Для-чего-нужна-identityhashmap)
+ [В чем разница между `HashMap` и `WeakHashMap`? Для чего используется `WeakHashMap`?](#В-чем-разница-между-hashmap-и-weakhashmap-Для-чего-используется-weakhashmap)
+ [В `WeakHashMap` используются WeakReferences. А почему бы не создать `SoftHashMap` на SoftReferences?](#В-weakhashmap-используются-weakreferences-А-почему-бы-не-создать-softhashmap-на-softreferences)
+ [В `WeakHashMap` используются WeakReferences. А почему бы не создать `PhantomHashMap` на PhantomReferences?](#В-weakhashmap-используются-weakreferences-А-почему-бы-не-создать-phantomhashmap-на-phantomreferences)
+ [`LinkedHashMap` - что в нем от `LinkedList`, а что от `HashMap`?](#linkedhashmap---что-в-нем-от-linkedlist-а-что-от-hashmap)
+ [В чем проявляется «сортированность» `SortedMap`, кроме того, что `toString()` выводит все элементы по порядку?](#В-чем-проявляется-сортированность-sortedmap-кроме-того-что-tostring-выводит-все-элементы-по-порядку)
+ [Как устроен `HashMap`?](#Как-устроен-hashmap)
+ [Согласно Кнуту и Кормену существует две основных реализации хэш-таблицы: на основе открытой адресации и на основе метода цепочек. Как реализована `HashMap`? Почему, по вашему мнению, была выбрана именно эта реализация? В чем плюсы и минусы каждого подхода?](#Согласно-Кнуту-и-Кормену-существует-две-основных-реализации-хэш-таблицы-на-основе-открытой-адресации-и-на-основе-метода-цепочек-Как-реализована-hashmap-Почему-по-вашему-мнению-была-выбрана-именно-эта-реализация-В-чем-плюсы-и-минусы-каждого-подхода)
+ [Как работает `HashMap` при попытке сохранить в него два элемента по ключам с одинаковым `hashCode()`, но для которых `equals() == false`?](#Как-работает-hashmap-при-попытке-сохранить-в-него-два-элемента-по-ключам-с-одинаковым-hashcode-но-для-которых-equals--false)
+ [Какое начальное количество корзин в `HashMap`?](#Какое-начальное-количество-корзин-в-hashmap)
+ [Какова оценка временной сложности операций над элементами из `HashMap`? Гарантирует ли `HashMap` указанную сложность выборки элемента?](#Какова-оценка-временной-сложности-операций-над-элементами-из-hashmap-Гарантирует-ли-hashmap-указанную-сложность-выборки-элемента)
+ [Возможна ли ситуация, когда `HashMap` выродится в список даже с ключами имеющими разные `hashCode()`?](#Возможна-ли-ситуация-когда-hashmap-выродится-в-список-даже-с-ключами-имеющими-разные-hashcode)
+ [В каком случае может быть потерян элемент в `HashMap`?](#В-каком-случае-может-быть-потерян-элемент-в-hashmap)
+ [Почему нельзя использовать `byte[]` в качестве ключа в `HashMap`?](#Почему-нельзя-использовать-byte-в-качестве-ключа-в-hashmap)
+ [Какова роль `equals()` и `hashCode()` в `HashMap`?](#Какова-роль-equals-и-hashcode-в-hashmap)
+ [Каково максимальное число значений `hashCode()`?](#Каково-максимальное-число-значений-hashcode)
+ [Какое худшее время работы метода get(key) для ключа, которого нет в `HashMap`?](#Какое-худшее-время-работы-метода-getkey-для-ключа-которого-нет-в-hashmap)
+ [Какое худшее время работы метода get(key) для ключа, который есть в `HashMap`?](#Какое-худшее-время-работы-метода-getkey-для-ключа-который-есть-в-hashmap)
+ [Сколько переходов происходит в момент вызова `HashMap.get(key)` по ключу, который есть в таблице?](#Сколько-переходов-происходит-в-момент-вызова-hashmapgetkey-по-ключу-который-есть-в-таблице)
+ [Сколько создается новых объектов, когда вы добавляете новый элемент в `HashMap`?](#Сколько-создается-новых-объектов-когда-вы-добавляете-новый-элемент-в-hashmap)
+ [Как и когда происходит увеличение количества корзин в `HashMap`?](#Как-и-когда-происходит-увеличение-количества-корзин-в-hashmap)
+ [Объясните смысл параметров в конструкторе `HashMap(int initialCapacity, float loadFactor)`.](#Объясните-смысл-параметров-в-конструкторе-hashmapint-initialcapacity-float-loadfactor)
+ [Будет ли работать `HashMap`, если все добавляемые ключи будут иметь одинаковый `hashCode()`?](#Будет-ли-работать-hashmap-если-все-добавляемые-ключи-будут-иметь-одинаковый-hashcode)
+ [Как перебрать все ключи `Map`?](#Как-перебрать-все-ключи-map)
+ [Как перебрать все значения `Map`?](#Как-перебрать-все-значения-map)
+ [Как перебрать все пары «ключ-значение» в `Map`?](#Как-перебрать-все-пары-ключ-значение-в-map)
+ [В чем отличия `TreeSet` и `HashSet`?](#В-чем-отличия-treeset-и-hashset)
+ [Что будет, если добавлять элементы в `TreeSet` по возрастанию?](#Что-будет-если-добавлять-элементы-в-treeset-по-возрастанию)
+ [Чем `LinkedHashSet` отличается от `HashSet`?](#Чем-linkedhashset-отличается-от-hashset)
+ [Для `Enum` есть специальный класс `java.util.EnumSet`. Зачем? Чем авторов не устраивал `HashSet` или `TreeSet`?](#Для-enum-есть-специальный-класс-javautilenumset-Зачем-Чем-авторов-не-устраивал-hashset-или-treeset)
+ [Какие существуют способы перебирать элементы списка?](#Какие-существуют-способы-перебирать-элементы-списка)
+ [Каким образом можно получить синхронизированные объекты стандартных коллекций?](#Каким-образом-можно-получить-синхронизированные-объекты-стандартных-коллекций)
+ [How `CopyOnWriteArrayList` and `CopyOnWriteArraySet` work?]()
+ [How `ConcurrentHashMap` works?]()
+ [What are key features of `ConcurrentHashMap` comparing to synchronized map?]()
+ [Please tell about java `BlockingQueue<E>` interface and its main implementations]()
+ [Please tell about java `ConcurrentNavigableMap<K,V>` interface and its main implementations]()
+ [Как получить коллекцию только для чтения?](#Как-получить-коллекцию-только-для-чтения)
+ [Напишите однопоточную программу, которая заставляет коллекцию выбросить `ConcurrentModificationException`.](#Напишите-однопоточную-программу-которая-заставляет-коллекцию-выбросить-concurrentmodificationexception)
+ [Приведите пример, когда какая-либо коллекция выбрасывает `UnsupportedOperationException`.](#Приведите-пример-когда-какая-либо-коллекция-выбрасывает-unsupportedoperationexception)
+ [Реализуйте симметрическую разность двух коллекций используя методы `Collection` (`addAll(...)`, `removeAll(...)`, `retainAll(...)`).](#Реализуйте-симметрическую-разность-двух-коллекций-используя-методы-collection-addall-removeall-retainall)
+ [Как, используя LinkedHashMap, сделать кэш c «invalidation policy»?](#Как-используя-linkedhashmap-сделать-кэш-c-invalidation-policy)
+ [Как одной строчкой скопировать элементы любой `collection` в массив?](#Как-одной-строчкой-скопировать-элементы-любой-collection-в-массив)
+ [Как одним вызовом из `List` получить `List` со всеми элементами, кроме первых и последних 3-х?](#Как-одним-вызовом-из-list-получить-list-со-всеми-элементами-кроме-первых-и-последних-3-х)
+ [Как одной строчкой преобразовать `HashSet` в `ArrayList`?](#Как-одной-строчкой-преобразовать-hashset-в-arraylist)
+ [Как одной строчкой преобразовать `ArrayList` в `HashSet`?](#Как-одной-строчкой-преобразовать-arraylist-в-hashset)
+ [Сделайте `HashSet` из ключей `HashMap`.](#Сделайте-hashset-из-ключей-hashmap)
+ [Сделайте `HashMap` из `HashSet<Map.Entry<K, V>>`.](#Сделайте-hashmap-из-hashsetmapentryk-v)

## Что такое _«коллекция»_?
_«Коллекция»_ - это структура данных, набор каких-либо объектов. Данными (объектами в наборе) могут быть числа, строки, объекты пользовательских классов и т.п.

[to the top](#java-collections-framework)

## Please describe main interfaces in JCF and their realizations
На вершине иерархии в Java Collection Framework располагаются 2 интерфейса:
`Collection` и `Map`. Эти интерфейсы разделяют все коллекции,
входящие во фреймворк на две части по типу хранения данных: 
простые последовательные наборы элементов и наборы пар «ключ — значение» соответственно.

Интерфейс `Collection` расширяют интерфейсы:

+ `List` (список) представляет собой коллекцию, в которой допустимы дублирующие значения. Реализации:
    + `ArrayList` - инкапсулирует в себе обычный массив, длина которого автоматически увеличивается при добавлении новых элементов. Элементы такой коллекции пронумерованы, начиная от нуля, к ним можно обратиться по индексу.
    + `LinkedList` (двунаправленный связный список) - состоит из узлов, каждый из которых содержит как собственно данные, так и две ссылки на следующий и предыдущий узел.
    + `Vector` — реализация динамического массива объектов, методы которой синхронизированы.
    + `Stack` — реализация стека LIFO (last-in-first-out).
+ `Set` (сет) описывает неупорядоченную коллекцию, не содержащую повторяющихся элементов. Реализации:
    + `HashSet` - использует HashMap для хранения данных. В качестве ключа используется добавляемый элемент, в качестве значения - заглушка Object. Из-за особенностей реализации порядок элементов не гарантируется при добавлении.
    + `LinkedHashSet` — гарантирует, что порядок элементов при обходе коллекции будет идентичен порядку добавления элементов.
    + `TreeSet` — предоставляет возможность управлять порядком элементов в коллекции при помощи объекта `Comparator`, либо сохраняет элементы с использованием «natural ordering».
+ `Queue` (очередь) предназначена для хранения элементов с предопределённым способом вставки и извлечения FIFO (first-in-first-out):
    + `PriorityQueue` — предоставляет возможность управлять порядком элементов в коллекции при помощи объекта `Comparator`, либо сохраняет элементы с использованием «natural ordering».
    + `ArrayDeque` — реализация интерфейса `Deque`, который расширяет интерфейс `Queue` методами, позволяющими реализовать конструкцию вида LIFO (last-in-first-out). 

Интерфейс `Map` реализован классами:

+ `Hashtable` — хэш-таблица, методы которой синхронизированы. Не позволяет использовать `null` в качестве значения или ключа и не является упорядоченной.
+ `HashMap` — хэш-таблица. Позволяет использовать `null` в качестве значения или ключа и не является упорядоченной.
+ `LinkedHashMap` — упорядоченная реализация хэш-таблицы.
+ `TreeMap` — реализация, основанная на красно-чёрных деревьях. Является упорядоченной и предоставляет возможность управлять порядком элементов в коллекции при помощи объекта `Comparator`, либо сохраняет элементы с использованием «natural ordering».
+ `WeakHashMap` — реализация хэш-таблицы, которая организована с использованием _weak references_ для ключей (сборщик мусора автоматически удалит элемент из коллекции при следующей сборке мусора, если на ключ этого элемента нет жёстких ссылок).

[to the top](#java-collections-framework))

## Расположите в виде иерархии следующие интерфейсы: `List`, `Set`, `Map`, `SortedSet`, `SortedMap`, `Collection`, `Iterable`, `Iterator`, `NavigableSet`, `NavigableMap`.
+ `Iterable`
    + `Collection`
        + `List`
        + `Set`
            + `SortedSet`
                + `NavigableSet`
+ `Map`
    + `SortedMap` 
        + `NavigableMap`
+ `Iterator`

[to the top](#java-collections-framework)

##  Why `Map` isn't related to `Collection` interface but `List` and `Set` are relate to `Collection`?
`Collection` stores only elements
`Map` - stores key-value pairs.

[to the top](#java-collections-framework)

## В чем разница между классами `java.util.Collection` и `java.util.Collections`?
`java.util.Collections` - набор статических методов для работы с коллекциями.

`java.util.Collection` - один из основных интерфейсов Java Collections Framework.

[to the top](#java-collections-framework)

## Что такое «fail-fast поведение»?
__fail-fast поведение__ означает, что при возникновении ошибки или состояния, которое может привести к ошибке, система немедленно прекращает дальнейшую работу и уведомляет об этом. Использование fail-fast подхода позволяет избежать недетерминированного поведения программы в течение времени.

В Java Collections API некоторые итераторы ведут себя как fail-fast и выбрасывают `ConcurrentModificationException`, если после его создания была произведена модификация коллекции, т.е. добавлен или удален элемент напрямую из коллекции, а не используя методы итератора. 

Реализация такого поведения осуществляется за счет подсчета количества модификаций коллекции (modification count):

+ при изменении коллекции счетчик модификаций так же изменяется;
+ при создании итератора ему передается текущее значение счетчика;
+ при каждом обращении к итератору сохраненное значение счетчика сравнивается с текущим, и, если они не совпадают, возникает исключение.

[to the top](#java-collections-framework)

## Какая разница между fail-fast и fail-safe?
В противоположность fail-fast, итераторы fail-safe не вызывают никаких исключений при изменении структуры, потому что они работают с клоном коллекции вместо оригинала.

[to the top](#java-collections-framework)

## Приведите примеры итераторов, реализующих поведение fail-safe
Итератор коллекции `CopyOnWriteArrayList` и итератор представления `keySet` коллекции `ConcurrentHashMap` являются примерами итераторов fail-safe.

[to the top](#java-collections-framework)

## Чем различаются `Enumeration` и `Iterator`.
Хотя оба интерфейса и предназначены для обхода коллекций между ними имеются существенные различия:

+ с помощью `Enumeration` нельзя добавлять/удалять элементы;
+ в `Iterator` исправлены имена методов для повышения читаемости кода (`Enumeration.hasMoreElements()` соответствует `Iterator.hasNext()`, `Enumeration.nextElement()` соответствует `Iterator.next()` и т.д);
+ `Enumeration` присутствуют в устаревших классах, таких как `Vector`/`Stack`, тогда как `Iterator` есть во всех современных классах-коллекциях. 

[to the top](#java-collections-framework)

## Как между собой связаны `Iterable` и `Iterator`?
Интерфейс `Iterable` имеет только один метод - `iterator()`, который возвращает `Iterator`.

[to the top](#java-collections-framework)

## Как между собой связаны `Iterable`, `Iterator` и «for-each»?
Классы, реализующие интерфейс `Iterable`, могут применяться в конструкции `for-each`, которая использует `Iterator`.

[to the top](#java-collections-framework)

## Сравните `Iterator` и `ListIterator`.
+ `ListIterator` расширяет интерфейс `Iterator`
+ `ListIterator` может быть использован только для перебора элементов коллекции `List`;
+ `Iterator` позволяет перебирать элементы только в одном направлении, при помощи метода `next()`. Тогда как `ListIterator` позволяет перебирать список в обоих направлениях, при помощи методов `next()` и `previous()`;
+ `ListIterator` не указывает на конкретный элемент: его текущая позиция располагается между элементами, которые возвращают методы `previous()` и `next()`.
+ При помощи `ListIterator` вы можете модифицировать список, добавляя/удаляя элементы с помощью методов `add()` и `remove()`. `Iterator` не поддерживает данного функционала.

[to the top](#java-collections-framework)

## Что произойдет при вызове `Iterator.next()` без предварительного вызова `Iterator.hasNext()`?
Если итератор указывает на последний элемент коллекции, то возникнет исключение `NoSuchElementException`, иначе будет возвращен следующий элемент.

[to the top](#java-collections-framework)

## Сколько элементов будет пропущено, если `Iterator.next()` будет вызван после 10-ти вызовов `Iterator.hasNext()`?
Нисколько - `hasNext()` осуществляет только проверку наличия следующего элемента.

[to the top](#java-collections-framework)

## Как поведёт себя коллекция, если вызвать `iterator.remove()`?
Если вызову `iterator.remove()` предшествовал вызов `iterator.next()`, то `iterator.remove()` удалит элемент коллекции, на который указывает итератор, в противном случае будет выброшено `IllegalStateException()`.

[to the top](#java-collections-framework)

## Как поведёт себя уже инстанциированный итератор для `collection`, если вызвать `collection.remove()`?
При следующем вызове методов итератора будет выброшено `ConcurrentModificationException`.

[to the top](#java-collections-framework)

## Как избежать `ConcurrentModificationException` во время перебора коллекции?
+ Попробовать подобрать или реализовать самостоятельно другой итератор, работающий по принципу fail-safe.
+ Использовать `ConcurrentHashMap` и `CopyOnWriteArrayList`.
+ Преобразовать список в массив и перебирать массив.
+ Блокировать изменения списка на время перебора с помощью блока `synchronized`.

Отрицательная сторона последних двух вариантов - ухудшение производительности.

[to the top](#java-collections-framework)

## Какая коллекция реализует дисциплину обслуживания FIFO?
FIFO, First-In-First-Out («первым пришел-первым ушел») - по этому принципу построена коллекция `Queue`.

[to the top](#java-collections-framework)

## Какая коллекция реализует дисциплину обслуживания FILO?
FILO, First-In-Last-Out («первым пришел, последним ушел») - по этому принципу построена коллекция `Stack`.

[to the top](#java-collections-framework)

## Чем отличается `ArrayList` от `Vector`?
## Зачем добавили `ArrayList`, если уже был `Vector`?
+ Методы класса `Vector` синхронизированы, а `ArrayList` - нет;
+ По умолчанию, `Vector` удваивает свой размер, когда заканчивается выделенная под элементы память. `ArrayList` же увеличивает свой размер только на половину.

`Vector` это устаревший класс и его использование не рекомендовано.

[to the top](#java-collections-framework)

## What is the difference between `ArrayList` and `LinkedList`? In which cases is it better to use `ArrayList`, and in which cases is `LinkedList`?
`ArrayList` is an implementation of `List` interface with dynamically re-sizing array, 
 `LinkedList` is an implementation with doubly-linked list

`ArrayList`:

+ `get(int index)` is O(1). **Main benefit** of `ArrayList<E>`;
+ `add(E element)` is O(1) amortized, but O(n) worst-case since the array must be resized and copied;
+ `add(int index, E element)` is O(n) (with n/2 steps on average) in this case, all the elements that are to the right of the element being added
are shifted one cell to the right
+ `remove(int index)` is O(n) (with n/2 steps on average) because at the same time, all elements located to the right of the element being deleted
are shifted one cell to the left (the actual size of the array (capacity) does not change);
+ `Iterator.remove()` is O(n) (with n/2 steps on average)
+ `ListIterator.add(E element)` is O(n) (with n/2 steps on average)
+ minimum overhead costs during storage.

Many of the operations need n/2 steps on average, constant number of steps in the best case (end of list), 
n steps in the worst case (start of list)

`LinkedList`:

+ `get(int index)` is O(n) (with n/4 steps on average), but O(1) when index = 0 or index = list.size() - 1 (in this case, you can also use `getFirst()` and `getLast()`).
One of the main benefits of `LinkedList<E>`;
+ `add(int index, E element)` is O(n) (with n/4 steps on average), but O(1) when `index = 0` or `index = list.size() - 1`
(in this case, you can also use `addFirst()` and `addLast()`/`add()`). One of the main benefits of `LinkedList<E>`
+ `remove(int index)` is O(n) (with n/4 steps on average), but O(1) when index = 0 or index = list.size() - 1 
(in this case, you can also use `removeFirst()` and `removeLast()`). Removing element by index takes a linear time because before deleting 
element we have to iterate to its position from top or from the bottom of the list(it takes linear time);
+ `Iterator.remove()` is O(1).
+ `ListIterator.add(E element)` is O(1).
+ consumes more memory than `ArrayList<E>` because stores references to previous and next elements

Many of the operations need n/4 steps on average, constant number of steps in the best case (e.g. index = 0), and n/2 steps in worst case (middle of list)
So, depending on the operations you intend to do, you should choose the implementations accordingly.
Iterating over either kind of List is practically equally cheap. 
Iterating over an ArrayList is technically faster, but unless you're doing something really performance-sensitive, 
you shouldn't worry about this -- they're both constants.

Also, if you have large lists, keep in mind that memory usage is also different. 
Each element of a LinkedList has more overhead since pointers to the next and previous elements are also stored.
`ArrayLists` don't have this overhead. However, `ArrayLists` take up as much memory as is allocated for the capacity, 
regardless of whether elements have actually been added.

**Summary** `ArrayList` with `ArrayDeque` are preferable in many more use-cases than `LinkedList`. If you're not sure — just start with `ArrayList`

[Stackoverflow1](https://stackoverflow.com/a/322742)
[Stackoverflow2](https://stackoverflow.com/a/7671021)

[to the top](#java-collections-framework)

## Что работает быстрее `ArrayList` или `LinkedList`?
Смотря какие действия будут выполняться над структурой. 

см. [Чем отличается `ArrayList` от `LinkedList`](#Чем-отличается-arraylist-от-linkedlist-В-каких-случаях-лучше-использовать-первый-а-в-каких-второй)

[to the top](#java-collections-framework)

## Какое худшее время работы метода `contains()` для элемента, который есть в `LinkedList`?
_O(N)_. Время поиска элемента линейно пропорционально количеству элементов в списке.

[to the top](#java-collections-framework)

## Какое худшее время работы метода `contains()` для элемента, который есть в `ArrayList`?
_O(N)_. Время поиска элемента линейно пропорционально количеству элементов с списке.

[to the top](#java-collections-framework)

## Какое худшее время работы метода `add()` для `LinkedList`?
_O(N)_. Добавление в начало/конец списка осуществляется за время _O(1)_.

[to the top](#java-collections-framework)

## Какое худшее время работы метода `add()` для `ArrayList`?
_O(N)_. Вставка элемента в конец списка осуществляется за время _O(1)_, но если вместимость массива недостаточна, то происходит создание нового массива с увеличенным размером и копирование всех элементов из старого массива в новый.

[to the top](#java-collections-framework)

## Необходимо добавить 1 млн. элементов, какую структуру вы используете?
Однозначный ответ можно дать только исходя из информации о том в какую часть списка происходит добавление элементов, что потом будет происходить с элементами списка, существуют ли какие-то ограничения по памяти или скорости выполнения.

см. [Чем отличается `ArrayList` от `LinkedList`](#Чем-отличается-arraylist-от-linkedlist-В-каких-случаях-лучше-использовать-первый-а-в-каких-второй)

[to the top](#java-collections-framework)

## Как происходит удаление элементов из `ArrayList`? Как меняется в этом случае размер `ArrayList`?

При удалении произвольного элемента из списка, все элементы, находящиеся «правее» смещаются на одну ячейку влево и реальный размер массива (его емкость, capacity) не изменяется никак. Механизм автоматического «расширения» массива существует, а вот автоматического «сжатия» нет, можно только явно выполнить «сжатие» командой `trimToSize()`.

[to the top](#java-collections-framework)

## Предложите эффективный алгоритм удаления нескольких рядом стоящих элементов из середины списка, реализуемого `ArrayList`.
Допустим нужно удалить `n` элементов с позиции `m` в списке. Вместо выполнения удаления одного элемента `n` раз (каждый раз смещая на 1 позицию элементы, стоящие «правее» в списке), нужно выполнить смещение всех элементов, стоящих «правее» `n + m` позиции на `n` элементов «левее» к началу списка. Таким образом, вместо выполнения `n` итераций перемещения элементов списка, все выполняется за 1 проход. Но если говорить об общей эффективности - то самый быстрый способ будет с использованием `System.arraycopy()`, и получить к нему доступ можно через метод - `subList(int fromIndex, int toIndex)`

Пример:

```java
import java.io.*;
import java.util.ArrayList;

public class Main {
    //позиция, с которой удаляем
    private static int m = 0;
    //количество удаляемых элементов
    private static int n = 0;
    //количество элементов в списке
    private static final int size = 1000000;
    //основной список (для удаления вызовом remove() и его копия для удаления путём перезаписи)
    private static ArrayList<Integer> initList, copyList;
    
    public static void main(String[] args){
        
        initList = new ArrayList<>(size);
        for (int i = 0; i < size; i++) {
            initList.add(i);
        }
        System.out.println("Список из 1.000.000 элементов заполнен");
        
        copyList = new ArrayList<>(initList);
        System.out.println("Создана копия списка\n");
        
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        try{
            System.out.print("С какой позиции удаляем? > ");
            m = Integer.parseInt(br.readLine());
            System.out.print("Сколько удаляем? > ");
            n = Integer.parseInt(br.readLine());
        } catch(IOException e){
            System.err.println(e.toString());
        }
        System.out.println("\nВыполняем удаление вызовом remove()...");
        long start = System.currentTimeMillis();
        
        for (int i = m - 1; i < m + n - 1; i++) {
            initList.remove(i);
        }
        
        long finish = System.currentTimeMillis() - start;
        System.out.println("Время удаления с помощью вызова remove(): " + finish);
        System.out.println("Размер исходного списка после удаления: " + initList.size());
        
        System.out.println("\nВыполняем удаление путем перезаписи...\n");
        start = System.currentTimeMillis();
        
        removeEfficiently();
        
        finish = System.currentTimeMillis() - start;
        System.out.println("Время удаления путём смещения: " + finish);
        System.out.println("Размер копии списка:" + copyList.size());

        System.out.println("\nВыполняем удаление через SubList...\n");
        start = System.currentTimeMillis();

        initList.subList(m - 1, m + n).clear();

        finish = System.currentTimeMillis() - start;
        System.out.println("Время удаления через саблист: " + finish);
        System.out.println("Размер копии списка:" + copyList.size());
    }
    
    private static void removeEfficiently(){
        /* если необходимо удалить все элементы, начиная с указанного,
         * то удаляем элементы с конца до m
         */
        if (m + n >= size){
            int i = size - 1;
            while (i != m - 1){
                copyList.remove(i);
                i--;
            }
        } else{
            //переменная k необходима для отсчёта сдвига начиная от места вставка m
            for (int i  = m + n, k = 0; i < size; i++, k++) {
               copyList.set(m + k, copyList.get(i));
            }
            
            /* удаляем ненужные элементы в конце списка
             * удаляется всегда последний элемент, так как время этого действия
             * фиксировано и не зависит от размера списка
             */
            int i = size - 1;
            while (i != size - n - 1){
                copyList.remove(i);
                i--;
            }
            //сокращаем длину списка путём удаления пустых ячеек
            copyList.trimToSize();
        }
    }
}
```

Результат выполнения:
```
run:
Список из 1.000.000 элементов заполнен
Создана копия списка

С какой позиции удаляем? > 600000
Сколько удаляем? > 20000

Выполняем удаление вызовом remove()...
Время удаления с помощью вызова remove(): 928
Размер исходного списка после удаления: 980000

Выполняем удаление путем перезаписи...

Время удаления путём смещения: 17
Размер копии списка:980000

Выполняем удаление через SubList...

Время удаления через саблист: 1
Размер копии списка:980000
СБОРКА УСПЕШНО ЗАВЕРШЕНА (общее время: 33 секунды)
```

[to the top](#java-collections-framework)

## Сколько необходимо дополнительной памяти при вызове `ArrayList.add()`?
Если в массиве достаточно места для размещения нового элемента, то дополнительной памяти не требуется. Иначе происходит создание нового массива размером в 1,5 раза превышающим существующий (это верно для JDK выше 1.7, в более ранних версиях размер увеличения иной).

[to the top](#java-collections-framework)

## Сколько выделяется дополнительно памяти при вызове `LinkedList.add()`?
Создается один новый экземпляр вложенного класса `Node`.

[to the top](#java-collections-framework)

## Оцените количество памяти на хранение одного примитива типа `byte` в `LinkedList`?
Каждый элемент `LinkedList` хранит ссылку на предыдущий элемент, следующий элемент и ссылку на данные.

```java
private static class Node<E> {
        E item;
        Node<E> next;
        Node<E> prev;
//...
}
```

Для 32-битных систем каждая ссылка занимает 32 бита (4 байта). Сам объект (заголовок) вложенного класса `Node` занимает 8 байт. 4 + 4 + 4 + 8 = 20 байт, а т.к. размер каждого объекта в Java кратен 8, соответственно получаем 24 байта. Примитив типа `byte` занимает 1 байт памяти, но в JCF примитивы упаковываются: объект типа `Byte` занимает в памяти 16 байт (8 байт на заголовок объекта, 1 байт на поле типа `byte` и 7 байт для кратности 8). Также напомню, что значения от -128 до 127 кэшируются и для них новые объекты каждый раз не создаются. Таким образом, в x32 JVM 24 байта тратятся на хранение одного элемента в списке и 16 байт - на хранение упакованного объекта типа `Byte`. Итого 40 байт.

Для 64-битной JVM каждая ссылка занимает 64 бита (8 байт), размер заголовка каждого объекта составляет 16 байт (два машинных слова). Вычисления аналогичны: 8 + 8 + 8 + 16 = 40байт и 24 байта. Итого 64 байта.

[to the top](#java-collections-framework)

## Оцените количество памяти на хранение одного примитива типа `byte` в `ArrayList`?
`ArrayList` основан на массиве, для примитивных типов данных осуществляется автоматическая упаковка значения, поэтому 16 байт тратится на хранение упакованного объекта и 4 байта (8 для x64) - на хранение ссылки на этот объект в самой структуре данных. Таким образом, в x32 JVM 4 байта используются на хранение одного элемента и 16 байт - на хранение упакованного объекта типа `Byte`. Для x64 - 8 байт и 24 байта соответственно.

[to the top](#java-collections-framework)

## Для `ArrayList` или для `LinkedList` операция добавления элемента в середину (`list.add(list.size()/2, newElement)`) медленнее?
Для `ArrayList`:

+ проверка массива на вместимость. Если вместимости недостаточно, то увеличение размера массива и копирование всех элементов в новый массив (_O(N)_);
+ копирование всех элементов, расположенных правее от позиции вставки, на одну позицию вправо (_O(N)_);
+ вставка элемента (_O(1)_).

Для `LinkedList`:

+ поиск позиции вставки (_O(N)_);
+ вставка элемента (_O(1)_).

В худшем случае вставка в середину списка эффективнее для `LinkedList`. В остальных - скорее всего, для `ArrayList`, поскольку копирование элементов осуществляется за счет вызова быстрого системного метода `System.arraycopy()`.

[to the top](#java-collections-framework)

## В реализации класса `ArrayList` есть следующие поля: `Object[] elementData`, `int size`. Объясните, зачем хранить отдельно `size`, если всегда можно взять `elementData.length`?
Размер массива `elementData` представляет собой вместимость (capacity) `ArrayList`, которая всегда больше переменной `size` - реального количества хранимых элементов. При необходимости вместимость автоматически возрастает.

[to the top](#java-collections-framework)

## Сравните интерфейсы `Queue` и `Deque`.
## Кто кого расширяет: `Queue` расширяет `Deque`, или `Deque` расширяет `Queue`?
`Queue` - это очередь, которая обычно (но необязательно) строится по принципу FIFO (First-In-First-Out) - соответственно извлечение элемента осуществляется с начала очереди, вставка элемента - в конец очереди. Хотя этот принцип нарушает, к примеру, `PriorityQueue`, использующая «natural ordering» или переданный `Comparator` при вставке нового элемента.

`Deque` (Double Ended Queue) расширяет `Queue` и согласно документации, это линейная коллекция, поддерживающая вставку/извлечение элементов с обоих концов. Помимо этого, реализации интерфейса `Deque` могут строится по принципу FIFO, либо LIFO.

Реализации и `Deque`, и `Queue` обычно не переопределяют методы `equals()` и `hashCode()`, вместо этого используются унаследованные методы класса Object, основанные на сравнении ссылок.

[to the top](#java-collections-framework)

## Почему `LinkedList` реализует и `List`, и `Deque`?
`LinkedList` позволяет добавлять элементы в начало и конец списка за константное время, что хорошо согласуется с поведением интерфейса `Deque`.

[to the top](#java-collections-framework)

## `LinkedList` — это односвязный, двусвязный или четырехсвязный список?
`Двусвязный`: каждый элемент `LinkedList` хранит ссылку на предыдущий и следующий элементы.

[to the top](#java-collections-framework)

## Как перебрать элементы `LinkedList` в обратном порядке, не используя медленный `get(index)`?
Для этого в `LinkedList` есть обратный итератор, который можно получить вызва метод `descendingIterator()`.

[to the top](#java-collections-framework)

## Что позволяет сделать `PriorityQueue`?
Особенностью `PriorityQueue` является возможность управления порядком элементов. По-умолчанию, элементы сортируются с использованием «natural ordering», но это поведение может быть переопределено при помощи объекта `Comparator`, который задаётся при создании очереди. Данная коллекция не поддерживает null в качестве элементов.

Используя `PriorityQueue`, можно, например, реализовать алгоритм Дейкстры для поиска кратчайшего пути от одной вершины графа к другой. Либо для хранения объектов согласно определённого свойства.

[to the top](#java-collections-framework)

## `Stack` считается «устаревшим». Чем его рекомендуют заменять? Почему?
`Stack` был добавлен в Java 1.0 как реализация стека LIFO (last-in-first-out) и является расширением коллекции `Vector`, хотя это несколько нарушает понятие стека (например, класс `Vector` предоставляет возможность обращаться к любому элементу по индексу). Является частично синхронизированной коллекцией (кроме метода добавления `push()`) с вытекающими отсюда последствиями в виде негативного воздействия на производительность. После добавления в Java 1.6 интерфейса `Deque`, рекомендуется использовать реализации именно этого интерфейса, например, `ArrayDeque`.

[to the top](#java-collections-framework)

## What are the differences between `HashMap` and `Hashtable`?
+ Методы класса `Hashtable` синхронизированы, что приводит к снижению производительности, а `HashMap` - нет;
+ `HashTable` не может содержать элементы `null`, тогда как `HashMap` может содержать один ключ `null` и любое количество значений `null`;
+ Iterator у `HashMap`, в отличие от Enumeration у `HashTable`, работает по принципу «fail-fast» (выдает исключение при любой несогласованности данных).

`Hashtable` это устаревший класс и его использование не рекомендовано.

[to the top](#java-collections-framework)

## В чем разница между `HashMap` и `IdentityHashMap`? Для чего нужна `IdentityHashMap`?
`IdentityHashMap` - это структура данных, так же реализующая интерфейс `Map` и использующая при сравнении ключей (значений) сравнение ссылок, а не вызов метода `equals()`. Другими словами, в `IdentityHashMap` два ключа `k1` и `k2` будут считаться равными, если они указывают на один объект, т.е. выполняется условие `k1` == `k2`.

`IdentityHashMap` не использует метод `hashCode()`, вместо которого применяется метод `System.identityHashCode()`, по этой причине `IdentityHashMap` по сравнению с `HashMap` имеет более высокую производительность, особенно если последний хранит объекты с дорогостоящими методами `equals()` и `hashCode()`.

Одним из основных требований к использованию `HashMap` является неизменяемость ключа, а, т.к. `IdentityHashMap` не использует методы  `equals()` и `hashCode()`, то это правило на него не распространяется.

`IdentityHashMap` может применяться для реализации сериализации/клонирования. При выполнении подобных алгоритмов программе необходимо обслуживать хэш-таблицу со всеми ссылками на объекты, которые уже были обработаны. Такая структура не должна рассматривать уникальные объекты как равные, даже если метод `equals()` возвращает `true`.

Пример кода:
```java
import java.util.HashMap;
import java.util.IdentityHashMap;
import java.util.Map;

public class Q2 {

    public static void main(String[] args) {
        Q2 q = new Q2();
        q.testHashMapAndIdentityHashMap();
    }

    private void testHashMapAndIdentityHashMap() {
        CreditCard visa = new CreditCard("VISA", "04/12/2019");

        Map<CreditCard, String> cardToExpiry = new HashMap<>();
        Map<CreditCard, String> cardToExpiryIdenity = new IdentityHashMap<>();

        System.out.println("adding to HM");
        // inserting objects to HashMap
        cardToExpiry.put(visa, visa.getExpiryDate());

        // inserting objects to IdentityHashMap
        cardToExpiryIdenity.put(visa, visa.getExpiryDate());
        System.out.println("adding to IHM");

        System.out.println("before modifying keys");
        String result = cardToExpiry.get(visa) != null ? "Yes" : "No";
        System.out.println("Does VISA card exists in HashMap? " + result);

        result = cardToExpiryIdenity.get(visa) != null ? "Yes" : "No";
        System.out.println("Does VISA card exists in IdenityHashMap? " + result);

        // modifying value object
        visa.setExpiryDate("02/11/2030");

        System.out.println("after modifying keys");
        result = cardToExpiry.get(visa) != null ? "Yes" : "No";
        System.out.println("Does VISA card exists in HashMap? " + result);

        result = cardToExpiryIdenity.get(visa) != null ? "Yes" : "No";
        System.out.println("Does VISA card exists in IdenityHashMap? " + result);

        System.out.println("cardToExpiry.containsKey");
        System.out.println(cardToExpiry.containsKey(visa));
        System.out.println("cardToExpiryIdenity.containsKey");
        System.out.println(cardToExpiryIdenity.containsKey(visa));
    }

}

class CreditCard {
    private String issuer;
    private String expiryDate;

    public CreditCard(String issuer, String expiryDate) {
        this.issuer = issuer;
        this.expiryDate = expiryDate;
    }

    public String getIssuer() {
        return issuer;
    }

    public String getExpiryDate() {
        return expiryDate;
    }

    public void setExpiryDate(String expiry) {
        this.expiryDate = expiry;
    }

    @Override
    public int hashCode() {
        final int prime = 31;
        int result = 1;
        result = prime * result + ((expiryDate == null) ? 0 : expiryDate.hashCode());
        result = prime * result + ((issuer == null) ? 0 : issuer.hashCode());
        System.out.println("hashCode = " + result);
        return result;
    }

    @Override
    public boolean equals(Object obj) {
        System.out.println("equals !!! ");
        if (this == obj)
            return true;
        if (obj == null)
            return false;
        if (getClass() != obj.getClass())
            return false;
        CreditCard other = (CreditCard) obj;
        if (expiryDate == null) {
            if (other.expiryDate != null)
                return false;
        } else if (!expiryDate.equals(other.expiryDate))
            return false;
        if (issuer == null) {
            if (other.issuer != null)
                return false;
        } else if (!issuer.equals(other.issuer))
            return false;
        return true;
    }

}
```

Результат выполнения кода:
```
adding to HM
hashCode = 1285631513
adding to IHM
before modifying keys
hashCode = 1285631513
Does VISA card exists in HashMap? Yes
Does VISA card exists in IdenityHashMap? Yes
after modifying keys
hashCode = 791156485
Does VISA card exists in HashMap? No
Does VISA card exists in IdenityHashMap? Yes
cardToExpiry.containsKey
hashCode = 791156485
false
cardToExpiryIdenity.containsKey
true
```

[to the top](#java-collections-framework)

## В чем разница между `HashMap` и `WeakHashMap`? Для чего используется `WeakHashMap`?
В Java существует 4 типа ссылок: _сильные (strong reference)_, _мягкие (SoftReference)_, _слабые (WeakReference)_ и _фантомные (PhantomReference)_. Особенности каждого типа ссылок связаны с работой Garbage Collector. Если объект можно достичь только с помощью цепочки WeakReference (то есть на него отсутствуют сильные и мягкие ссылки), то данный объект будет помечен на удаление.

`WeakHashMap` - это структура данных, реализующая интерфейс `Map` и основанная на использовании WeakReference для хранения ключей. Таким образом, пара «ключ-значение» будет удалена из `WeakHashMap`, если на объект-ключ более не имеется сильных ссылок.

В качестве примера использования такой структуры данных можно привести следующую ситуацию: допустим имеются объекты, которые необходимо расширить дополнительной информацией, при этом изменение класса этих объектов нежелательно либо невозможно. В этом случае добавляем каждый объект в `WeakHashMap` в качестве ключа, а в качестве значения - нужную информацию. Таким образом, пока на объект имеется сильная ссылка (либо мягкая), можно проверять хэш-таблицу и извлекать информацию. Как только объект будет удален, то WeakReference для этого ключа будет помещен в ReferenceQueue и затем соответствующая запись для этой слабой ссылки будет удалена из `WeakHashMap`.

[to the top](#java-collections-framework)

## В `WeakHashMap` используются WeakReferences. А почему бы не создать `SoftHashMap` на SoftReferences?
`SoftHashMap` представлена в сторонних библиотеках, например, в `Apache Commons`.

[to the top](#java-collections-framework)

## В `WeakHashMap` используются WeakReferences. А почему бы не создать `PhantomHashMap` на PhantomReferences?
PhantomReference при вызове метода `get()` возвращает всегда `null`, поэтому тяжело представить назначение такой структуры данных.

[to the top](#java-collections-framework)

## `LinkedHashMap` - что в нем от `LinkedList`, а что от `HashMap`?
Реализация `LinkedHashMap` отличается от `HashMap` поддержкой двухсвязанного списка, определяющего порядок итерации по элементам структуры данных. По умолчанию элементы списка упорядочены согласно их порядку добавления в `LinkedHashMap` (insertion-order). Однако порядок итерации можно изменить, установив параметр конструктора `accessOrder` в значение `true`. В этом случае доступ осуществляется по порядку последнего обращения к элементу (access-order). Это означает, что при вызове методов `get()` или `put()` элемент, к которому обращаемся, перемещается в конец списка.

При добавлении элемента, который уже присутствует в `LinkedHashMap` (т.е. с одинаковым ключом), порядок итерации по элементам не изменяется.

[to the top](#java-collections-framework)

## В чем проявляется «сортированность» `SortedMap`, кроме того, что `toString()` выводит все элементы по порядку?
Так же оно проявляется при итерации по коллекции.

[to the top](#java-collections-framework)

## How does `HashMap` work? And what it's internal structure?
`HashMap` consists of buckets. 
From the technical point of view buckets are elements of an array, 
which stores references to singly linked lists of elements. 
When you add new key-value pair to `HashMap` the hash code of key is calculatedПри добавлении новой пары «ключ-значение», вычисляет хэш-код ключа,
based on which the number of the bucket (the number of the array cell)
into which the new element adds is calculated. If the bucket is empty, then it is saved
a link to the newly added element, if there is already an element there, then there
is a sequential iteration on the links between the elements in the chain, in search of the last
element, from which the link to the newly added element is placed.
If an item with the same key was found in the list, it is replaced.

[to the top](#java-collections-framework)

## Согласно Кнуту и Кормену существует две основных реализации хэш-таблицы: на основе открытой адресации и на основе метода цепочек. Как реализована `HashMap`? Почему, по вашему мнению, была выбрана именно эта реализация? В чем плюсы и минусы каждого подхода?
`HashMap` реализован с использованием метода цепочек, т.е. каждой ячейке массива (корзине) соответствует свой связный список и при возникновении коллизии осуществляется добавление нового элемента в этот список.

Для метода цепочек коэффициент заполнения может быть больше 1 и с увеличением числа элементов производительность убывает линейно. Такие таблицы удобно использовать, если заранее неизвестно количество хранимых элементов, либо их может быть достаточно много, что приводит к большим значениям коэффициента заполнения.

Среди методов открытой реализации различают:

+ линейное пробирование;
+ квадратичное пробирование;
+ двойное хэширование.

Недостатки структур с методом открытой адресации:

+ Количество элементов в хэш-таблице не может превышать размера массива. По мере увеличения числа элементов и повышения коэффициента заполнения производительность структуры резко падает, поэтому необходимо проводить перехэширование.
+ Сложно организовать удаление элемента.
+ Первые два метода открытой адресации приводят к проблеме первичной и вторичной группировок.

Преимущества хэш-таблицы с открытой адресацией: 

+ отсутствие затрат на создание и хранение объектов списка; 
+ простота организации сериализации/десериализации объекта.

[to the top](#java-collections-framework)

## Как работает `HashMap` при попытке сохранить в него два элемента по ключам с одинаковым `hashCode()`, но для которых `equals() == false`?
По значению `hashCode()` вычисляется индекс ячейки массива, в список которой этот элемент будет добавлен. Перед добавлением осуществляется проверка на наличие элементов в этой ячейке. Если элементы с таким `hashCode()` уже присутствует, но их `equals()` методы не равны, то элемент будет добавлен в конец списка.

[to the top](#java-collections-framework)

## Какое начальное количество корзин в `HashMap`?
В конструкторе по умолчанию - 16, используя конструкторы с параметрами можно задавать произвольное начальное количество корзин.

[to the top](#java-collections-framework)

## Какова оценка временной сложности операций над элементами из `HashMap`? Гарантирует ли `HashMap` указанную сложность выборки элемента?
В общем случае операции добавления, поиска и удаления элементов занимают константное время. 

Данная сложность не гарантируется, т.к. если хэш-функция распределяет элементы по корзинам равномерно, временная сложность станет не хуже [_Логарифмического времени_ ](https://ru.wikipedia.org/wiki/%D0%92%D1%80%D0%B5%D0%BC%D0%B5%D0%BD%D0%BD%D0%B0%D1%8F_%D1%81%D0%BB%D0%BE%D0%B6%D0%BD%D0%BE%D1%81%D1%82%D1%8C_%D0%B0%D0%BB%D0%B3%D0%BE%D1%80%D0%B8%D1%82%D0%BC%D0%B0#%D0%9B%D0%BE%D0%B3%D0%B0%D1%80%D0%B8%D1%84%D0%BC%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%BE%D0%B5_%D0%B2%D1%80%D0%B5%D0%BC%D1%8F) O(log(N)), а в случае, когда хэш-функция постоянно возвращает одно и то же значение, `HashMap` превратится в связный список со сложностью О(n).

Пример кода двоичного поиска:
```java
public class Q {
    public static void main(String[] args) {
        Q q = new Q();
        q.binSearch();
    }

    private void binSearch() {
        int[] inpArr = {1, 2, 3, 4, 5, 6, 7, 8, 9};
        Integer result = binSearchF(inpArr, 1, 0, inpArr.length - 1);
        System.out.println("-----------------------");
        result = binSearchF(inpArr, 2, 0, inpArr.length - 1);
        System.out.println("Found at position " + result);
    }

    private Integer binSearchF(int[] inpArr, int searchValue, int low, int high) {
        Integer index = null;
        while (low <= high) {
            System.out.println("New iteration, low = " + low + ", high = " + high);
            int mid = (low + high) / 2;
            System.out.println("trying mid = " + mid + " inpArr[mid] = " + inpArr[mid]);
            if (inpArr[mid] < searchValue) {
                low = mid + 1;
                System.out.println("inpArr[mid] (" + inpArr[mid] + ") < searchValue(" + searchValue + "), mid = " + mid
                        + ", setting low = " + low);
            } else if (inpArr[mid] > searchValue) {
                high = mid - 1;
                System.out.println("inpArr[mid] (" + inpArr[mid] + ") > searchValue(" + searchValue + "), mid = " + mid
                        + ", setting high = " + high);
            } else if (inpArr[mid] == searchValue) {
                index = mid;
                System.out.println("found at index " + mid);
                break;
            }
        }
        return index;
    }
}
```

[to the top](#java-collections-framework)

## Возможна ли ситуация, когда `HashMap` выродится в список даже с ключами имеющими разные `hashCode()`?
Это возможно в случае, если метод, определяющий номер корзины будет возвращать одинаковые значения.

[to the top](#java-collections-framework)

## В каком случае может быть потерян элемент в `HashMap`?
Допустим, в качестве ключа используется не примитив, а объект с несколькими полями. После добавления элемента в `HashMap` у объекта, который выступает в качестве ключа, изменяют одно поле, которое участвует в вычислении хэш-кода. В результате при попытке найти данный элемент по исходному ключу, будет происходить обращение к правильной корзине, а вот `equals` уже не найдет указанный ключ в списке элементов. Тем не менее, даже если `equals` реализован таким образом, что изменение данного поля объекта не влияет на результат, то после увеличения размера корзин и пересчета хэш-кодов элементов, указанный элемент, с измененным значением поля, с большой долей вероятности попадет в совершенно другую корзину и тогда уже потеряется совсем.

[to the top](#java-collections-framework)

## Почему нельзя использовать `byte[]` в качестве ключа в `HashMap`?
Хэш-код массива не зависит от хранимых в нем элементов, а присваивается при создании массива (метод вычисления хэш-кода массива не переопределен и вычисляется по стандартному `Object.hashCode()` на основании адреса массива). Так же у массивов не переопределен `equals` и выполняется сравнение указателей. Это приводит к тому, что обратиться к сохраненному с ключом-массивом элементу не получится при использовании другого массива такого же размера и с такими же элементами, доступ можно осуществить лишь в одном случае — при использовании той же самой ссылки на массив, что использовалась для сохранения элемента.

[to the top](#java-collections-framework)

## Какова роль `equals()` и `hashCode()` в `HashMap`?
`hashCode` позволяет определить корзину для поиска элемента, а `equals` используется для сравнения ключей элементов в списке корзины и искомого ключа.

[to the top](#java-collections-framework)

## Каково максимальное число значений `hashCode()`?
Число значений следует из сигнатуры `int hashCode()` и равно диапазону типа `int` — __2<sup>32</sup>__.

[to the top](#java-collections-framework)

## Какое худшее время работы метода get(key) для ключа, которого нет в `HashMap`?
## Какое худшее время работы метода get(key) для ключа, который есть в `HashMap`?
___O(N)___. Худший случай - это поиск ключа в `HashMap`, вырожденного в список по причине совпадения ключей по `hashCode()` и для выяснения хранится ли элемент с определённым ключом может потребоваться перебор всего списка.

Но начиная с Java 8, после определенного числа элементов в списке, связный список преобразовывается в красно-черное дерево и сложность выборки, даже в случае плохой хеш-функции, не хуже _логарифмической_ _O(log(N))_

[to the top](#java-collections-framework)

## Сколько переходов происходит в момент вызова `HashMap.get(key)` по ключу, который есть в таблице?
+ ключ равен `null`: __1__ - выполняется единственный метод `getForNullKey()`.
+ любой ключ отличный от `null`: __4__ - вычисление хэш-кода ключа; определение номера корзины; поиск значения; возврат значения.

[to the top](#java-collections-framework)

## Сколько создается новых объектов, когда вы добавляете новый элемент в `HashMap`?
__Один__ новый объект статического вложенного класса `Entry<K,V>`.

[to the top](#java-collections-framework)

## Как и когда происходит увеличение количества корзин в `HashMap`?
Помимо `capacity` у `HashMap` есть еще поле `loadFactor`, на основании которого, вычисляется предельное количество занятых корзин `capacity * loadFactor`. По умолчанию `loadFactor = 0.75`. По достижению предельного значения, число корзин увеличивается в 2 раза и для всех хранимых элементов вычисляется новое «местоположение» с учетом нового числа корзин.

[to the top](#java-collections-framework)

## Объясните смысл параметров в конструкторе `HashMap(int initialCapacity, float loadFactor)`.
+ `initialCapacity` - исходный размер `HashMap`, количество корзин в хэш-таблице в момент её создания.
+ `loadFactor` - коэффициент заполнения `HashMap`, при превышении которого происходит увеличение количества корзин и автоматическое перехэширование. Равен отношению числа уже хранимых элементов в таблице к её размеру. 

[to the top](#java-collections-framework)
## Почему количество корзин в `HashMap`(_capacity_) всегда равняется  2<sup>n</sup>
`HashMap` определяет в какую корзину положить любой переданный ключ, делая мапинг `int` на значение в диапазоне `[0, capacity]`.
Когда `capacity` является степенью двух, эту операцию можно провести очень оптимально с точки зрения производительности. 
При инициализации `HashMap`, размер ячеек в ней вычисляется внутри конструктора с помощью 
`this.threshold = tableSizeFor(initialCapacity);`
Метод `tableSizeFor()`:
```java
static final int tableSizeFor(int cap) {
        int n = -1 >>> Integer.numberOfLeadingZeros(cap - 1);
        return (n < 0) ? 1 : (n >= MAXIMUM_CAPACITY) ? MAXIMUM_CAPACITY : n + 1;
    }
```
Первая строчка в методе вычисляет ближайшее число к переменной `cap`, которое в двоичном представлении состоит только из 1,
то есть данное число представляет собой число вида _2<sup>n</sup>-1_, затем к нашему числу прибавляется 1, чтобы получить число вида
2<sup>n</sup>, оно и будет являться реальной `capacity` данной `HashMap`

Таким образом, объект `HashMap` невозможно инициализировать с `capcity`, которая не является числом вида 2<sup>n</sup>, 
более того, ее невозможно реализовать по-другому, так как индекс(позиция) элемента вычисляется по 
выражению `(n - 1) & hash` если число n является 2<sup>m</sup>, то `n - 1` в двоичном представлении будет представлять число только из 1 и при
выполнении операции побитового "И" мы получим последние m бит от числа `hash` и тогда индекс корзины может представлять собой любое число 
от 0 до `n - 1`, если `capacity` будет равна, например 3, тогда `(n - 1) & hash` может быть равен 0 или 2, в корзину с номером 1
будет невозможно добавить элемент.

[источник](https://stackoverflow.com/a/53526992)

[исходный код](https://github.com/openjdk/jdk/blob/master/src/java.base/share/classes/java/util/HashMap.java)

[to the top](#java-collections-framework)
## Что происходит внутри корзины в `HashMap`, когда количество элементов в ней становится большим?
Если речь идет о `HashMap`, в java 7 и более старых версиях, то при увеличении числа элементов внутри корзины они так и 
хранятся в виде односвязного списка, если количество элементов во `HashMap` становится больше чем `capacity * loadFactor`, то 
тогда происходит вызов `resize()` и элементы перераспределяются по корзинам `HashMap`, но все также в случае коллизий
хранятся в виде односвязного списка внутри корзины.

В java 8 и выше, когда количество элементов в корзине становится больше 8(`TREEIFY_THRESHOLD`), то они
начинают храниться в виде красно-черного дерева, данная трансформация происходит, если общее количество корзин в `HashMap`
больше 64(`MIN_TREEFY_CAPCITY`). При использовании `HashMap` лучше, чтобы ключи были `Comparable`, если это не так, то 
используется метод `compareTo` для имен классов двух сравниваемых объектов, если он возвращает 0, то сравнение происходит 
с использованием `System.identityHashCode()` 

[Источник_1](https://stackoverflow.com/a/43911638)
[источник_2](https://stackoverflow.com/questions/47921663/when-and-how-does-hashmap-convert-the-bucket-from-linked-list-to-red-black-trees)

[to the top](#java-collections-framework)
## Что такое `TREEIFY_THRESHOLD` `MIN_TREEFY_CAPCITY` `UNTREEIFY_THRESHOLD`?

```java
static final int TREEIFY_THRESHOLD = 8;
static final int UNTREEIFY_THRESHOLD = 6;
static final int MIN_TREEIFY_CAPACITY = 64;
```
Данные поля пришли с выходом java 8 и появлением в ней новой оптимизации связанной с хранением элементов в одной корзине 
внутри `HashMap`, когда элементы внутри корзины хранятся в виде красно-черного дерева при увеличении их количества больше определенного значения(`TREEIFY_THRESHOLD`),
так как размер массива корзин внутри `HashMap` может увеличиваться и количество элементов внутри одной корзины, как правило,
уменьшается ниже определенного значения(`UNTREEIFY_THRESHOLD`), то тогда они перестают храниться в виде дерева.

`MIN_TREEIFY_CAPACITY` - минимальное количество корзин в `HashMap`, когда начинает применяться оптимизация по представлению 
элементов в одной ячейке в виде красно-черного дерева.
 
[источник](https://stackoverflow.com/a/43911638)

[to the top](#java-collections-framework)
## Как работает `System.identityHashCode()`?
Точное поведение данного метода зависит от конкретной реализации JVM. Значение, которое возвращает `identityHashCode()` 
_гарантированно не изменится_ на протяжении всего срока жизни объекта, это означает, что если объект будет перемещен сборщиком мусора, 
то значение не поменяется, так как оно не зависит от адреса объекта в памяти.

`identityHashCode()` проверяет есть ли у данного объекта уже созданное значение `identityHashCode` и возвращает его, если оно 
есть. Если нет, то генерирует случайное число используя генератор регистра сдвига Джорджа Марсалья. 

[источник 1](https://stackoverflow.com/a/4933258)
[источник 2](https://stackoverflow.com/a/4933404)

[to the top](#java-collections-framework)
## Будет ли работать `HashMap`, если все добавляемые ключи будут иметь одинаковый `hashCode()`?
Да, будет, но в этом случае `HashMap` вырождается в связный список и теряет свои преимущества.

## Как перебрать все ключи `Map`?
Использовать метод `keySet()`, который возвращает множество `Set<K>` ключей.

[to the top](#java-collections-framework)

## Как перебрать все значения `Map`?
Использовать метод `values()`, который возвращает коллекцию `Collection<V>` значений.

[to the top](#java-collections-framework)

## Как перебрать все пары «ключ-значение» в `Map`?
Использовать метод `entrySet()`, который возвращает множество `Set<Map.Entry<K, V>` пар «ключ-значение».

[to the top](#java-collections-framework)

## В чем отличия `TreeSet` и `HashSet`?
`TreeSet` обеспечивает упорядоченно хранение элементов в виде красно-черного дерева. Сложность выполнения основных операций не хуже _O(log(N))_ (_Логарифмическое время_). 

`HashSet` использует для хранения элементов такой же подход, что и `HashMap`, за тем отличием, что в `HashSet` в качестве ключа и значения выступает сам `элемент`, кроме того, `HashSet` не поддерживает упорядоченное хранение элементов и обеспечивает временную сложность выполнения операций аналогично `HashMap`.

[to the top](#java-collections-framework)

## Что будет, если добавлять элементы в `TreeSet` по возрастанию?
В основе `TreeSet` лежит красно-черное дерево, которое умеет само себя балансировать. В итоге, `TreeSet` все равно в каком порядке вы добавляете в него элементы, преимущества этой структуры данных будут сохраняться.

[to the top](#java-collections-framework)

## Чем `LinkedHashSet` отличается от `HashSet`?
`LinkedHashSet` отличается от `HashSet` только тем, что в его основе лежит `LinkedHashMap` вместо `HashMap`. Благодаря этому порядок элементов при обходе коллекции является идентичным порядку добавления элементов (insertion-order). При добавлении элемента, который уже присутствует в `LinkedHashSet` (т.е. с одинаковым ключом), порядок обхода элементов не изменяется.

[to the top](#java-collections-framework)

## Для `Enum` есть специальный класс `java.util.EnumSet`. Зачем? Чем авторов не устраивал `HashSet` или `TreeSet`?
`EnumSet` - это реализация интерфейса `Set` для использования с перечислениями (`Enum`). В структуре данных хранятся объекты только одного типа `Enum`, указываемого при создании. Для хранения значений `EnumSet` использует массив битов (_bit vector_), - это позволяет получить высокую компактность и эффективность. Проход по `EnumSet` осуществляется согласно порядку объявления элементов перечисления. 

Все основные операции выполняются за _O(1)_ и обычно (но негарантированно) быстрей аналогов из `HashSet`, а пакетные операции (_bulk operations_), такие как `containsAll()` и `retainAll()` выполняются даже гораздо быстрей. 

Помимо всего `EnumSet` предоставляет множество статических методов инициализации для упрощенного и удобного создания экземпляров.

[to the top](#java-collections-framework)

## Какие существуют способы перебирать элементы списка?
+ Цикл с итератором

```java
Iterator<String> iterator = list.iterator();
while (iterator.hasNext()) {
    //iterator.next();
}
```

+ Цикл `for`

```java
for (int i = 0; i < list.size(); i++) {
    //list.get(i);
}
```

+ Цикл `while`

```java
int i = 0;
while (i < list.size()) {
    //list.get(i);
    i++;
}
```

+ «for-each»

```java
for (String element : list) {
    //element;
}
```

[to the top](#java-collections-framework)

## Каким образом можно получить синхронизированные объекты стандартных коллекций?
С помощью статических методов `synchronizedMap()` и `synchronizedList()` класса `Collections`. Данные методы возвращают синхронизированный декоратор переданной коллекции. При этом все равно в случае обхода по коллекции требуется ручная синхронизация. 

```java
  Map m = Collections.synchronizedMap(new HashMap());
  List l = Collections.synchronizedList(new ArrayList());
```

Начиная с Java 6 JCF был расширен специальными коллекциями, поддерживающими многопоточный доступ, такими как `CopyOnWriteArrayList` и `ConcurrentHashMap`.

[to the top](#java-collections-framework)



## Как получить коллекцию только для чтения?
При помощи:

+ `Collections.unmodifiableList(list)`;
+ `Collections.unmodifiableSet(set)`;
+ `Collections.unmodifiableMap(map)`.

Эти методы принимают коллекцию в качестве параметра, и возвращают коллекцию только для чтения с теми же элементами внутри.

[to the top](#java-collections-framework)

## Напишите однопоточную программу, которая заставляет коллекцию выбросить `ConcurrentModificationException`.
```java
public static void main(String[] args) {
    List<Integer> list = new ArrayList<>();
    list.add(1);
    list.add(2);
    list.add(3);

    for (Integer integer : list) {
        list.remove(1);
    }
}
```

[to the top](#java-collections-framework)

## Приведите пример, когда какая-либо коллекция выбрасывает `UnsupportedOperationException`.
```java
public static void main(String[] args) {
    List<Integer> list = Collections.emptyList();
    list.add(0);
}
```

[to the top](#java-collections-framework)

## Реализуйте симметрическую разность двух коллекций используя методы `Collection` (`addAll(...)`, `removeAll(...)`, `retainAll(...)`).
Симметрическая разность двух коллекций - это множество элементов, одновременно не принадлежащих обоим исходным коллекциям.

```java
<T> Collection<T> symmetricDifference(Collection<T> a, Collection<T> b) {    
    // Объединяем коллекции.
    Collection<T> result = new ArrayList<>(a);
    result.addAll(b);
    
    // Получаем пересечение коллекций.
    Collection<T> intersection = new ArrayList<>(a);
    intersection.retainAll(b);
    
    // Удаляем элементы, расположенные в обоих коллекциях.
    result.removeAll(intersection);

    return result;
}
```
[to the top](#java-collections-framework)

## Как, используя LinkedHashMap, сделать кэш c «invalidation policy»?
Необходимо использовать _LRU-алгоритм (Least Recently Used algorithm)_ и `LinkedHashMap` с access-order. В этом случае при обращении к элементу он будет перемещаться в конец списка, а наименее используемые элементы будут постепенно группироваться в начале списка. Так же в стандартной реализации `LinkedHashMap` есть метод `removeEldestEntries()`, который возвращает `true`, если текущий объект `LinkedHashMap` должен удалить наименее используемый элемент из коллекции при использовании методов `put()` и `putAll()`.

```java
public class LRUCache<K, V> extends LinkedHashMap<K, V> {
    private static final int MAX_ENTRIES = 10;

    public LRUCache(int initialCapacity) {
        super(initialCapacity, 0.85f, true);
    }

    @Override
    protected boolean removeEldestEntry(Map.Entry<K, V> eldest) {
        return size() > MAX_ENTRIES;
    }
}
```

Стоит заметить, что `LinkedHashMap` не позволяет полностью реализовать LRU-алгоритм, поскольку при вставке уже имеющегося в коллекции элемента порядок итерации по элементам не меняется.

[to the top](#java-collections-framework)

## Как одной строчкой скопировать элементы любой `collection` в массив?
```java
Object[] array = collection.toArray();
```

[to the top](#java-collections-framework)

## Как одним вызовом из `List` получить `List` со всеми элементами, кроме первых и последних 3-х?
```java
List<Integer> subList = list.subList(3, list.size() - 3);
```

[to the top](#java-collections-framework)

## Как одной строчкой преобразовать `HashSet` в `ArrayList`?
```java
ArrayList<Integer> list = new ArrayList<>(new HashSet<>());
```

[to the top](#java-collections-framework)

## Как одной строчкой преобразовать `ArrayList` в `HashSet`?
```java
HashSet<Integer> set = new HashSet<>(new ArrayList<>());
```

[to the top](#java-collections-framework)

## Сделайте `HashSet` из ключей `HashMap`.
```java
HashSet<Object> set = new HashSet<>(map.keySet());
```

[to the top](#java-collections-framework)

## Сделайте `HashMap` из `HashSet<Map.Entry<K, V>>`.
```java
HashMap<K, V> map = new HashMap<>(set.size());
for (Map.Entry<K, V> entry : set) {
    map.put(entry.getKey(), entry.getValue());
}
```

[to the top](#java-collections-framework)

# Источник
+ [parshinpn.pro](http://www.parshinpn.pro/content/voprosy-i-otvety-na-sobesedovanii-po-teme-java-collection-framework-chast-1)
+ [Хабрахабр](https://habrahabr.ru/post/162017/)
+ [Quizful](http://www.quizful.net/interview/java)
+ [JavaRush](http://info.javarush.ru/)
+ [Хабрахабр:Справочник по Java Collections Framework](https://habrahabr.ru/post/237043/)

[Вопросы для собеседования](README.md)

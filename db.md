[Вопросы для собеседования](README.md)

# Databases
+ [Что такое _«база данных»_?](#what-is-database)
+ [Что такое _«система управления базами данных»_?](#what-is-database-management-system-dbms)
+ [Что такое _«реляционная модель данных»_?](#what-is-relational-data-model)
+ [What is the difference between OLTP and OLAP databases?](#what-is-the-difference-between-oltp-and-olap-databases)
+ [Дайте определение терминам _«простой»_, _«составной» (composite)_, _«потенциальный» (candidate)_ и _«альтернативный» (alternate)_ ключ.](#define-the-terms-simple-key-composite-key-candidate-key-и-alternate-key)
+ [Что такое _«первичный ключ» (primary key)_? Каковы критерии его выбора?](#Что-такое-первичный-ключ-primary-key-Каковы-критерии-его-выбора)
+ [Что такое _«внешний ключ» (foreign key)_?](#Что-такое-внешний-ключ-foreign-key)
+ [Что такое _«нормализация»_?](#Что-такое-нормализация)
+ [Какие существуют нормальные формы?](#Какие-существуют-нормальные-формы)
+ [Что такое _«денормализация»_? Для чего она применяется?](#Что-такое-денормализация-Для-чего-она-применяется)
+ [Какие существуют типы связей в базе данных? Приведите примеры.](#Какие-существуют-типы-связей-в-базе-данных-Приведите-примеры)
+ [Что такое _«индексы»_? Для чего их используют? В чём заключаются их преимущества и недостатки?](#Что-такое-индексы-Для-чего-их-используют-В-чём-заключаются-их-преимущества-и-недостатки)
+ [Какие типы индексов существуют?](#Какие-типы-индексов-существуют)
+ [В чем отличие между кластерными и некластерными индексами?](#В-чем-отличие-между-кластерными-и-некластерными-индексами)
+ [Имеет ли смысл индексировать данные, имеющие небольшое количество возможных значений?](#Имеет-ли-смысл-индексировать-данные-имеющие-небольшое-количество-возможных-значений)
+ [Когда полное сканирование набора данных выгоднее доступа по индексу?](#Когда-полное-сканирование-набора-данных-выгоднее-доступа-по-индексу)
+ [Что такое _«транзакция»_?](#Что-такое-транзакция)
+ [Назовите основные свойства транзакции.](#Назовите-основные-свойства-транзакции)
+ [Какие существуют уровни изолированности транзакций?](#Какие-существуют-уровни-изолированности-транзакций)
+ [Какие проблемы могут возникать при параллельном доступе с использованием транзакций?](#Какие-проблемы-могут-возникать-при-параллельном-доступе-с-использованием-транзакций)
+ [What's the difference between optimistic and pessimistic locking?](#whats-the-difference-between-optimistic-and-pessimistic-locking)
+ [Tell about the terms of replication, partitioning and sharding in distributed data persistence systems](#tell-about-the-terms-of-replication-partitioning-and-sharding-in-distributed-data-persistence-systems)
+ [What are advantages and disadvantages of sharding?](#what-are-advantages-and-disadvantages-of-sharding)
+ [What are advantages and disadvantages of data replication?](#what-are-advantages-and-disadvantages-of-data-replication)


## What is database?
__Database__ is an organized collection of data stored and accessed electronically through the 
use of database management system

[Table of contents](#databases)

## What is database management system (DBMS)?
__Database management system (DBMS)__ is the software that interacts with end users, application, 
and the database itself to capture and analyze the data.

Main functions of the DBMS:

+ Data storage management 
+ Data transformation and presentation
+ Backup and recovery management
+ Security management

[Table of contents](#databases)

## What is relational data model?
__Relational data model__ is an approach to managing data using a structure and language consistent with 
first-order predicate logic

Relational model concepts:

+ **Attribute** — properties which define a relation
+ **Tables** Relations are saved in the table format, it stored along with entities
+ **Tuple** It's a single row of a table, which contains a single record
- **Relation schema** A relation schema represents the name of the relation with its attributes
+ **Attribute domain** Every attribute has some pre-defined value and scope which is known as attribute domain

[Table of contents](#databases)

## What is the difference between OLTP and OLAP databases?
- **OLTP**(On-line Transaction Processing) is involved in the operation of a particular system. OLTP 
is characterized by a large number of short on-line transactions (INSERT, UPDATE, DELETE). 
- The main purpose of OLTP systems is put on very fast query processing, maintaining data integrity in multi-access environments
- Effectiveness measured by number of transactions per second
- In OLTP database there is detailed and current data, and schema used to store transactional databases is 
the entity model(usually 3NF)
- **OLAP**(On-line Analytical Processing) deals with historical data or archival data. 
- OLAP is characterized by relatively low volume of transactions, queries are often very complex and involve aggregations
- For OLAP _response time_ is an effectiveness measure.  

[Table of contents](#databases)

## Define the terms: _simple key_, _composite key_, _candidate key_ и _alternate key_.
__Simple key__ consist of a single field to uniquely identify a record.
__Composite key__ - 2 or more keys

__Candidate key__ - simple or least composite key, which uniquely identifies each record in the table.

From all _candidate keys_ choose one and call it **primary key** all other keys called _alternative keys_

[Table of contents](#databases)

## Что такое _«первичный ключ» (primary key)_? Каковы критерии его выбора?
__Первичный ключ (primary key)__ в реляционной модели данных один из _потенциальных ключей_ отношения, выбранный в качестве основного ключа (ключа по умолчанию).

Если в отношении имеется единственный потенциальный ключ, он является и первичным ключом. Если потенциальных ключей несколько, один из них выбирается в качестве первичного, а другие называют _«альтернативными»_.

В качестве первичного обычно выбирается тот из потенциальных ключей, который наиболее удобен. Поэтому в качестве первичного ключа, как правило, выбирают тот, который имеет наименьший размер (физического хранения) и/или включает наименьшее количество атрибутов. Другой критерий выбора первичного ключа — сохранение его уникальности со временем. Поэтому в качестве первичного ключа стараются выбирать такой потенциальный ключ, который с наибольшей вероятностью никогда не утратит уникальность.

[Table of contents](#databases)

## Что такое _«внешний ключ» (foreign key)_?
__Внешний ключ (foreign key)__ — подмножество атрибутов некоторого отношения A, значения которых должны совпадать со значениями некоторого потенциального ключа некоторого отношения B.

[Table of contents](#databases)

## Что такое _«нормализация»_?
_Нормализация_ - это процесс преобразования отношений базы данных к виду, отвечающему нормальным формам (пошаговый, обратимый процесс замены исходной схемы другой схемой, в которой наборы данных имеют более простую и логичную структуру).

Нормализация предназначена для приведения структуры базы данных к виду, обеспечивающему минимальную логическую избыточность, и не имеет целью уменьшение или увеличение производительности работы или же уменьшение или увеличение физического объёма базы данных. Конечной целью нормализации является уменьшение потенциальной противоречивости хранимой в базе данных информации.

[Table of contents](#databases)

## Какие существуют нормальные формы?
__Первая нормальная форма (1NF)__ - Отношение находится в 1NF, если значения всех его атрибутов атомарны (неделимы). 

__Вторая нормальная форма (2NF)__ - Отношение находится в 2NF, если оно находится в 1NF, и при этом все неключевые атрибуты зависят только от ключа целиком, а не от какой-то его части.

__Третья нормальная форма (3NF)__ - Отношение находится в 3NF, если оно находится в 2NF и все неключевые атрибуты не зависят друг от друга.

__Четвёртая нормальная форма (4NF)__ - Отношение находится в 4NF , если оно находится в 3NF и если в нем не содержатся независимые группы атрибутов, между которыми существует отношение «многие-ко-многим».

__Пятая нормальная форма (5NF)__ - Отношение находится в 5NF, когда каждая нетривиальная зависимость соединения в ней определяется потенциальным ключом (ключами) этого отношения.

__Шестая нормальная форма (6NF)__ - Отношение находится в 6NF, когда она удовлетворяет всем нетривиальным зависимостям соединения, т.е. когда она неприводима, то есть не может быть подвергнута дальнейшей декомпозиции без потерь. Каждая переменная отношения, которая находится в 6NF, также находится и в 5NF. Введена как обобщение пятой нормальной формы для хронологической базы данных.

__Нормальная форма Бойса-Кодда, усиленная 3 нормальная форма (BCNF)__ - Отношение находится в BCNF, когда каждая её нетривиальная и неприводимая слева функциональная зависимость имеет в качестве своего детерминанта некоторый потенциальный ключ.

__Доменно-ключевая нормальная форма (DKNF)__ -  Отношение находится в DKNF, когда каждое наложенное на неё ограничение является логическим следствием ограничений доменов и ограничений ключей, наложенных на данное отношение.

[Table of contents](#databases)

## Give an example of violation of the 1NF
1NF means:
- Each table cell should contain a single value
- Each record needs to be unique.

For example, we have a table in database for storing rented movies for some user which violates 1NF

| Full name | Physical address | Movies rented|
|-----------|------------------|--------------|
| Janet Jones|First st Plot no 4|Ted, Cars|
| Robert Phill| 3rd street 34|Forgetting Satah, Fractured|


## Give an example of violation only of 2NF
2NF means:
- Table in 1NF
- All non-key attributes are fully dependent on a primary key

| Full name | Physical address     | Movies rented| Number of customers |
|-----------|----------------------|--------------|---------------------|
| Janet Jones| First st Plot no 4   |Ted, Cars| 4                   |
| Robert Phill| 3rd street 34        |Forgetting Satah, Fractured| 5                   |

Here we add _Number of customers_ to count quantity of our customers in some building, but as we have composite 
primary key(Full name & Physical address), our column _Number of customers_ is dependent only on _Physical
address_ field, so we break 2NF

[Table of contents](#databases)

## Give an example of violation only of the 3NF

3NF means:
- Table in 2NF
- Table don't have transitive functional dependencies

| Full name | Physical address     | Movies rented| Number of movies rented |
|-----------|----------------------|--------------|-------------------------|
| Janet Jones| First st Plot no 4   |Ted, Cars| 2                       |
| Robert Phill| 3rd street 34        |Forgetting Satah, Fractured| 2                       |

Here we have _number of movies rented_ column which depends on _movies rented_ column

[Table of contents](#databases)

## Что такое _«денормализация»_? Для чего она применяется?
__Денормализация базы данных__ — это процесс осознанного приведения базы данных к виду, в котором она не будет соответствовать правилам нормализации. Обычно это необходимо для повышения производительности и скорости извлечения данных, за счет увеличения избыточности данных.

[Table of contents](#databases)

## Какие существуют типы связей в базе данных? Приведите примеры.
+ __Один к одному__ - любому значению атрибута А соответствует только одно значение атрибута В, и наоборот.

>Каждый университет гарантированно имеет 1-го ректора: _1 университет → 1 ректор_.

+ __Один ко многим__ - любому значению атрибута А соответствует 0, 1 или несколько значений атрибута В.

>В каждом университете есть несколько факультетов: _1 университет → много факультетов_.

+ __Многие ко многим__ - любому значению атрибута А соответствует 0, 1 или несколько значений атрибута В, и любому значению атрибута В соответствует 0, 1 или несколько значение атрибута А.

>1 профессор может преподавать на нескольких факультетах, в то же время на 1-ом факультете может преподавать несколько профессоров: _Несколько профессоров ↔ Несколько факультетов_.

[Table of contents](#databases)

## What is an index in DB? What are their advantages and disadvantages?
**Database index** is a data structure that improves the speed of data
retrieval operations on a database table at the cost of additional writes
and storage space to maintain the index data structure.
Indexes are used to quickly locate data without having to search every row
in a database table every time said table is accessed.

We need indexes because they allow us to highly optimize reading load in our database.
searching on a field that isn’t sorted requires a Linear Search which requires **(N+1)/2** block accesses (on average),
where N is the number of blocks that the table spans. If that field is a non-key field (i.e. doesn’t contain unique entries)
then the entire tablespace must be searched at **N** block accesses.
Whereas with a sorted field.
Whereas with a sorted field, a Binary Search may be used, which has `log2 N` block accesses.
Also since the data is sorted given a non-key field, the rest of the table doesn’t need to be searched for duplicate values,
once a higher value is found

Advantages

+ speed up the search and sorting by a specific field or set of fields.

Disadvantages 

+ The index itself occupies space on disk and memory (when used). So, if space or memory are issues then too many indexes could be a problem.
+ When data is inserted/updated/deleted, then the index needs to be maintained as well as the original data. This slows down updates and locks the tables (or parts of the tables), which can affect query processing

Indexes are preferable for:

+ The fields by which the data is sorted;
+ for any column that is being used as a foreign key into another table - add an index. It can either be a single column index - or it might be a compound index - whatever works best for your case. It's important that the foreign key column be the first column in that index (if you're using a compound index) - otherwise, the benefits for the JOIN's or for checking referential integrity won't be available to your system
+ For primary key (in some databases it is created by default, for example Oracle, SQL Server, and PostgreSQL);
+ Fields in which data is selected from a certain range. In this case, as soon as the first record with the desired value is found, all subsequent values will be located side by side.

Using indexes is impractical for:

+ Fields that are rarely used in read queries;
+ Fields that contain only two or three values, for example: _"yes"_, _"no"_.

[Stackoverflow](https://stackoverflow.com/a/11985423)

[Stackoverflow](https://stackoverflow.com/a/1130)

[Table of contents](#databases)

## What types of indexes exist?

__By sorting order__
+ _oredered_ — indexes in which the elements are ordered;
  + _ascending_;
  + _descending_;
+ _non-ordered_ — indexes in which the elements are unordered.

__By the impact on the data source__
+ _Clustered index_ -  is an index that physically reorganizes the order in which the data entries are stored and gives the maximum speedup.
  The logical structure of the dataset in this case is more of a dictionary than an index.
  The data in the dictionary is physically ordered, for example alphabetically.
  Cluster indexes can provide a significant increase in data retrieval performance, even compared to conventional indexes.
  The performance increase is especially noticeable when working with sequential data. There can be only one clustered index
+ _non-clustered index_ — the most typical representatives of the indexes. 
A non-clustered index doesn't change the physical structure of a dataset, but only organizes references to the corresponding entries
  To identify the desired record in the dataset, the non-cluster index organizes special pointers, including: 
information about the identification number of the file in which the record is stored; the identification number of the page of the corresponding data;
the number of the desired record on the corresponding page; the contents of the column.
  
It is generally faster to read from a clustered index if you want to get back all the columns. You do not have to go first to the index and then to the table.
Writing to a table with a clustered index can be slower, if there is a need to rearrange the data


__By storing structure__
+ _B-Tree_ - a B-tree stores data such that each node contains keys in ascending order.
Each of these keys has two references to another two child nodes. 
The left side child node keys are less than the current keys, 
and the right side child node keys are more than the current keys
+ _Hash_ - index based on a **hash function**. This function converts any database value to a numeric value called hash code
+ _GiST_ (Generalized Search Tree Indexes) - it's a family of indexes based on
a concurrent and recoverable height-balanced search tree infrastructure without making any 
assumptions about the type of data being stored, or the queries being serviced. Often severe as
base for indexes based on B+ trees, R-trees, hB-trees, RD-trees and other
+ _SP-GiST_ - like GiST indexes, offer an infrastructure that supports 
various kinds of searches. SP-GiST permits implementation of a wide range of different 
non-balanced disk-based data structures, such as quadtrees, k-d trees, and radix trees (tries)
+ _GIN_
+ _BRIN_

__По количественному составу__
+ _простой индекс (индекс с одним ключом)_ — строится по одному полю;
+ _составной (многоключевой, композитный) индекс_ — строится по нескольким полям при этом важен порядок их следования;
+ _индекс с включенными столбцами_ — некластеризованный индекс, дополнительно содержащий кроме ключевых столбцов еще и неключевые;
+ _главный индекс (индекс по первичному ключу)_ — это тот индексный ключ, под управлением которого в данный момент находится набор данных. Набор данных не может быть отсортирован по нескольким индексным ключам одновременно. Хотя, если один и тот же набор данных открыт одновременно в нескольких рабочих областях, то у каждой копии набора данных может быть назначен свой главный индекс.

__По характеристике содержимого__
+ _уникальный индекс_ состоит из множества уникальных значений поля;
+ _плотный индекс_ (NoSQL) — индекс, при котором, каждом документе в индексируемой коллекции соответствует запись в индексе, даже если в документе нет индексируемого поля.
+ _разреженный индекс_ (NoSQL) — тот, в котором представлены только те документы, для которых индексируемый ключ имеет какое-то определённое значение (существует).
+ _пространственный индекс_ — оптимизирован для описания географического местоположения. Представляет из себя многоключевой индекс состоящий из широты и долготы.
+ _составной пространственный индекс_ — индекс, включающий в себя кроме широты и долготы ещё какие-либо мета-данные (например теги). Но географические координаты должны стоять на первом месте.
+ _полнотекстовый (инвертированный) индекс_ — словарь, в котором перечислены все слова и указано, в каких местах они встречаются. При наличии такого индекса достаточно осуществить поиск нужных слов в нём и тогда сразу же будет получен список документов, в которых они встречаются.
+ _хэш-индекс_ предполагает хранение не самих значений, а их хэшей, благодаря чему уменьшается размер (а, соответственно, и увеличивается скорость их обработки) индексов из больших полей. Таким образом, при запросах с использованием хэш-индексов, сравниваться будут не искомое со значения поля, а хэш от искомого значения с хэшами полей.
Из-за нелинейнойсти хэш-функций данный индекс нельзя сортировать по значению, что приводит к невозможности использования в сравнениях больше/меньше и «is null». Кроме того, так как хэши не уникальны, то для совпадающих хэшей применяются методы разрешения коллизий.
+ _битовый индекс (bitmap index)_ — метод битовых индексов заключается в создании отдельных битовых карт (последовательностей 0 и 1) для каждого возможного значения столбца, где каждому биту соответствует запись с индексируемым значением, а его значение равное 1 означает, что запись, соответствующая позиции бита содержит индексируемое значение для данного столбца или свойства.
+ _обратный индекс (reverse index)_ — B-tree индекс, но с реверсированным ключом, используемый в основном для монотонно возрастающих значений (например, автоинкрементный идентификатор) в OLTP системах с целью снятия конкуренции за последний листовой блок индекса, т.к. благодаря переворачиванию значения две соседние записи индекса попадают в разные блоки индекса. Он не может использоваться для диапазонного поиска.
+ _функциональный индекс, индекс по вычисляемому полю (function-based index)_ — индекс, ключи которого хранят результат пользовательских функций. Функциональные индексы часто строятся для полей, значения которых проходят предварительную обработку перед сравнением в команде SQL. Например, при сравнении строковых данных без учета регистра символов часто используется функция UPPER. Кроме того, функциональный индекс может помочь реализовать любой другой отсутствующий тип индексов данной СУБД.
+ _первичный индекс_ — уникальный индекс по полю первичного ключа.
+ _вторичный индекс_ — индекс по другим полям (кроме поля первичного ключа).
+ _XML-индекс_ — вырезанное материализованное представление больших двоичных XML-объектов (BLOB) в столбце с типом данных xml.

__По механизму обновления__
+ _полностью перестраиваемый_ — при добавлении элемента заново перестраивается весь индекс.
+ _пополняемый (балансируемый)_ — при добавлении элементов индекс перестраивается частично (например, одна из ветви) и периодически балансируется.

__По покрытию индексируемого содержимого__
+ _полностью покрывающий (полный) индекс_ — покрывает всё содержимое индексируемого объекта.
+ _частичный индекс (partial index)_ — это индекс, построенный на части набора данных, удовлетворяющей определенному условию самого индекса. Данный индекс создан для уменьшения размера индекса.
+ _инкрементный (delta) индекс_ — индексируется малая часть данных(дельта), как правило, по истечении определённого времени. Используется при интенсивной записи. Например, полный индекс перестраивается раз в сутки, а дельта-индекс строится каждый час. По сути это частичный индекс по временной метке.
+ _индекс реального времени (real-time index)_ — особый вид инкрементного индекса, характеризующийся высокой скоростью построения. Предназначен для часто меняющихся данных.

__Индексы в кластерных системах__
+ _глобальный индекс_ — индекс по всему содержимому всех сегментов БД (shard).
+ _сегментный индекс_ — глобальный индекс по полю-сегментируемому ключу (shard key). Используется для быстрого определения сегмента, на котором хранятся данные в процессе маршрутизации запроса в кластере БД.
+ _локальный индекс_ —  индекс по содержимому только одного сегмента БД.

[Postgres docs](https://www.postgresql.org/docs/current/indexes-intro.html)
[Hyperskill topic](https://www.postgresql.org/docs/current/indexes-intro.html)
[Hyperskill topic composite indexes](https://hyperskill.org/learn/step/18011)
[What do Clustered and Non-Clustered index actually mean?](https://stackoverflow.com/questions/1251636/what-do-clustered-and-non-clustered-index-actually-mean?noredirect=1&lq=1)

[Table of contents](#databases)

## В чем отличие между кластерными и некластерными индексами?
Некластерные индексы - данные физически расположены в произвольном порядке, но логически упорядочены согласно индексу. Такой тип индексов подходит для часто изменяемого набора данных.

При кластерном индексировании данные физически упорядочены, что серьезно повышает скорость выборок данных (но только в случае последовательного доступа к данным). Для одного набора данных может быть создан только один кластерный индекс.

[Table of contents](#databases)

## What is the B-tree index and how it works?
B-Tree is the most common type of index. This index is based on a
balanced tree that maintains data sorted according to a specified condition
The B-Tree index is a family of indexes based on balanced trees. 
Depending on the particular database use, there can be a B+ Tree 
(which is an advanced form of B-Tree) or a Binary Tree (which is the simplest form of B-Tree),
or something else. This choice primarily affects the performance of the database, 
but the way how we use the index always remains the same

The top node is the root, and those below it are either child nodes or leaf nodes.
We always start searching for our row from the root node. 
We compare if the value we’re searching for is less than or greater 
than the value in the node at hand. The result of the comparison tells 
us which way to go, left or right, depending on the result of our comparison.

Adding a new element takes more time. When we insert new element it has to be inserted somewhere in the tree,
and the structure of this binary tree might change significantly to preserve the balance.
In this case creation of a new record in the database will take more time compared to the 
time required for this operation without indexes.
B-Tree indexes are not limited to working with numbers only. 
They can be used with dates, times, strings, and other ordered data types.
However, there is an important limitation when working with strings and B-Tree indexes:
the equality operator works only from the leftmost part of a string _(e.g. "c...", "ca..", "cat...")_
in alphabetical order.  So, if you search for all strings that match the pattern like "..cat..", your index won't work

[Table of contents](#databases)

## What is hash index and how it works?
The hash index is based on a hash function. 
This function converts any database value to a numeric value called hash code. 
Once you have a query that uses comparison by this value, 
the database doesn't have to scan the entire dataset to find the match. 
Instead, it will calculate the hash of the value used in the query condition 
and directly access that place where data with the same hash is stored.
In postgreSQL and some other popular DBs hash indexes store a 32-bit hash code derived from the value of the 
indexed column.

Hash indexes can potentially outperform B-Tree indexes when you need to find data 
by a specific key. However, they are way less popular in practice because they can be 
used only with equality operators and don't work with comparisons (<, >, <=, >=) and
sortings. Moreover, not all databases support hash indexes

[Table of contents](#databases)

## Имеет ли смысл индексировать данные, имеющие небольшое количество возможных значений?
Примерное правило, которым можно руководствоваться при создании индекса - если объем информации (в байтах) НЕ удовлетворяющей условию выборки меньше, чем размер индекса (в байтах) по данному условию выборки, то в общем случае оптимизация приведет к замедлению выборки.

[Table of contents](#databases)

## Когда полное сканирование набора данных выгоднее доступа по индексу?
Полное сканирование производится многоблочным чтением. Сканирование по индексу - одноблочным. Также, при доступе по индексу сначала идет сканирование самого индекса, а затем чтение блоков из набора данных. Число блоков, которые надо при этом прочитать из набора зависит от фактора кластеризации. Если суммарная стоимость всех необходимых одноблочных чтений больше стоимости полного сканирования многоблочным чтением, то полное сканирование выгоднее, и оно выбирается оптимизатором.

Таким образом, полное сканирование выбирается при слабой селективности предикатов запроса и/или слабой кластеризации данных, либо в случае очень маленьких наборов данных.

[Table of contents](#databases)

## Что такое _«транзакция»_?
__Транзакция__ - это воздействие на базу данных, переводящее её из одного целостного состояния в другое и выражаемое в изменении данных,
хранящихся в базе данных.

[Table of contents](#databases)

## Назовите основные свойства транзакции.
__Атомарность (atomicity)__ гарантирует, что никакая транзакция не будет зафиксирована в системе частично. Будут либо выполнены все её подоперации, либо не выполнено ни одной. 

__Согласованность (consistency)__. Транзакция, достигающая своего нормального завершения и, тем самым, фиксирующая свои результаты, сохраняет согласованность базы данных.

__Изолированность (isolation)__. Во время выполнения транзакции параллельные транзакции не должны оказывать влияние на её результат.

__Долговечность (durability)__. Независимо от проблем на нижних уровнях (к примеру, обесточивание системы или сбои в оборудовании) изменения, сделанные успешно завершённой транзакцией, должны остаться сохранёнными после возвращения системы в работу.

[Table of contents](#databases)

## Какие существуют уровни изолированности транзакций?
В порядке увеличения изолированности транзакций и, соответственно, надёжности работы с данными:

+ __Чтение неподтверждённых данных (грязное чтение) (read uncommitted, dirty read)__ — чтение незафиксированных изменений как своей транзакции, так и параллельных транзакций. Нет гарантии, что данные, изменённые другими транзакциями, не будут в любой момент изменены в результате их отката, поэтому такое чтение является потенциальным источником ошибок. Невозможны потерянные изменения, возможны неповторяемое чтение и фантомы.
+ __Чтение подтверждённых данных (read committed)__ — чтение всех изменений своей транзакции и зафиксированных изменений параллельных транзакций. Потерянные изменения и грязное чтение не допускается, возможны неповторяемое чтение и фантомы.
+ __Повторяемость чтения (repeatable read, snapshot)__ — чтение всех изменений своей транзакции, любые изменения, внесённые параллельными транзакциями после начала своей, недоступны. Потерянные изменения, грязное и неповторяемое чтение невозможны, возможны фантомы.
+ __Упорядочиваемость (serializable)__ — результат параллельного выполнения сериализуемой транзакции с другими транзакциями должен быть логически эквивалентен результату их какого-либо последовательного выполнения. Проблемы синхронизации не возникают.

[Table of contents](#databases)

## Какие проблемы могут возникать при параллельном доступе с использованием транзакций?
При параллельном выполнении транзакций возможны следующие проблемы:

+ __Потерянное обновление (lost update)__ — при одновременном изменении одного блока данных разными транзакциями одно из изменений теряется;
+ __«Грязное» чтение (dirty read)__ — чтение данных, добавленных или изменённых транзакцией, которая впоследствии не подтвердится (откатится);
+ __Неповторяющееся чтение (non-repeatable read)__ — при повторном чтении в рамках одной транзакции ранее прочитанные данные оказываются изменёнными;
+ __Фантомное чтение (phantom reads)__ — одна транзакция в ходе своего выполнения несколько раз выбирает множество записей по одним и тем же критериям. Другая транзакция в интервалах между этими выборками добавляет или удаляет записи или изменяет столбцы некоторых записей, используемых в критериях выборки первой транзакции, и успешно заканчивается. В результате получится, что одни и те же выборки в первой транзакции дают разные множества записей. 
Предположим, имеется две транзакции, открытые различными приложениями, в которых выполнены следующие SQL-операторы:

| Транзакция 1 |	Транзакция 2 |
|--------------|--------------|
| | SELECT SUM(f2) FROM tbl1; |
| INSERT INTO tbl1 (f1,f2) VALUES (15,20);	| |
| COMMIT;	| |
| | SELECT SUM(f2) FROM tbl1;|

В транзакции 2 выполняется SQL-оператор, использующий все значения поля f2. Затем в транзакции 1 выполняется вставка новой строки, приводящая к тому, что повторное выполнение SQL-оператора в транзакции 2 выдаст другой результат. Такая ситуация называется чтением фантома (фантомным чтением). От неповторяющегося чтения оно отличается тем, что результат повторного обращения к данным изменился не из-за изменения/удаления самих этих данных, а из-за появления новых (фантомных) данных.

[Table of contents](#databases)

## What's the difference between optimistic and pessimistic locking?

**Optimistic locking** is a strategy where you read a record, take note of a version number(other methods may involve
dates, timestamps or checksums) and check that the version hasn't changed before you write the record back.
When you write record back you filter the update on the version to make sure its atomic and update the version 
in one hit.

If the record is dirty(different version with yours) you abort the transaction and the user can restart it.

**Pessimistic locking** is when you lock the record for your exclusive use until you have finished with it.
It has much better integrity than optimistic locking but requires you to be careful with your application 
design to avoid deadlocks

[StackOverflow](https://stackoverflow.com/a/129397/22463602)

[Table of contents](#databases)

## Tell about the terms of replication, partitioning and sharding in distributed data persistence systems
**Replication**(Copying data) - keeping a copy of same data on multiple servers that are connected via a network

**Partitioning** - splitting up a large monolithic database into multiple smaller databases based on data cohesion.
There are 2 possible types when we want to split data is **horizontal(sharding)** and vertical(improve server hardware)

**Sharding**(Horizontal partitioning) - a type of horizontal partitioning that splits large
databases into smaller components, which are faster and easier to manage

[Table of contents](#databases)

## What are advantages and disadvantages of sharding?
- **Solve scalability issue**. With a single database server architecture any application experiences performance 
degradation, database sharding fixes all these issues by partitioning the dat across multiple machines
- **High availability**. If something happens to one of the servers in shared architecture, then only specific
shards will be down
- **Speed up query response time**
- **More write bandwidth** 

Disadvantages:
- **Adds complexity in the system**
- **Rebalancing data** Sometimes shards become unbalanced (when a shard outgrows other shards) and may create a 
_database hotspot_
- **Joining data from multiple shards is expensive** In shared architecture, you need to pull the data from different
shards, and you need to perform joins across multiple networked servers, it adds **latency**

[Table of contents](#databases)

## What are advantages and disadvantages of data replication?

- Keep data geographically close to users (reduces latency)
- Allow the system to continue working even if some of its parts have failed (increase availability)
- Scale number of servers that can serve read queries

Disadvantages:
- Concurrency is difficult to achieve in full replication
- Slow update because single update must be performed at different databases to keep the copies consistent

[Table of contents](#databases)

# Источники
+ [Википедия](https://ru.wikipedia.org/wiki/)
+ [tokarchuk.ru](http://tokarchuk.ru/2012/08/indexes-classification/)
+ [Quizful](http://www.quizful.net/interview/sql/)

[Вопросы для собеседования](README.md)

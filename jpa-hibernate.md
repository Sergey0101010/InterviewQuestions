# JPA, Hibernate, Spring Data

## What is JPA?
Java Persistance API - is a specification for managing data persistence in Java applications. JPA is used to
simplify the process of writing code for data persistence by providing high-level abstraction layer over 
the underlying data storage technology, such as relational databases.

## What is Hibernate and how it related to JPA?
Hibernate is the most popular ORM framework which implements JPA specification.

## What are entities in JPA?
In JPA entity is a java class that represents a persisted data object. Entities are used to map java objects 
to database tables where each entity corresponds to a row in the table.

To mark some class as entity you need to:
- Add `@Entity` annotation on top of the class
- entity class must have an `@Id` field
- `public` or `protected` no-args constructor
- Class can't be `final` and any of methods can't be `final`
getters and setters for all fields. 
- Must be top level class

To persist entities in the database JPA _EntityManager_ used, its an interface which provides CRUD methods
for entities.

## How to define relationships between entities in JPA?
To define relations between tables you use 3 types of annotations:
- `@OneToOne`
- `@OneToMany`
- `@ManyToMany`

## Give an example of `@OneToOne` Jpa relationship
```java
@Entity
public class Library {
    @Id
    @GeneratedValue
    private long id;
    
    @Column
    private String name;
    
    @OneToOne
    @JoinColumn(name = "address_id")
    private Address address;
    
    // constructor getters and setters
}
```

```java
@Entity
public class Address {
    @Id
    @GeneratedValue
    private long id;
    
    @Column(nullable = false)
    private String location;
    
    @OneToOne(mappedBy = "address")
    private Library library;
}
```
## Give an example of `@OneToMany` Jpa relationship

```java
@Entity
public class Book {

    @Id
    @GeneratedValue
    private long id;
    
    @Column(nullable=false)
    private String title;
    
    @ManyToOne
    @JoinColumn(name="library_id")
    private Library library;
    
    // standard constructor, getter, setter
}
```

```java
public class Library {
 
    //...
 
    @OneToMany(mappedBy = "library")
    private List<Book> books;
 
    //...
 
}
```

## Give an example of `@ManyToMany` Jpa relationship
```java
@Entity
public class Author {

    @Id
    @GeneratedValue
    private long id;

    @Column(nullable = false)
    private String name;

    @ManyToMany(cascade = CascadeType.ALL)
    @JoinTable(name = "book_author", 
      joinColumns = @JoinColumn(name = "book_id", referencedColumnName = "id"), 
      inverseJoinColumns = @JoinColumn(name = "author_id", 
      referencedColumnName = "id"))
    private List<Book> books;

    //standard constructors, getters, setters
}
```

```java
public class Book {
 
    //...
 
    @ManyToMany(mappedBy = "books")
    private List<Author> authors;
 
    //...
}
```

## What is JPQL?
JPQL - **Java Persistence Query Language** it's a platform independent object-oriented query language 
that is used to retrieve data from a relational database using JPA. JPQL is similar to SQL in syntax, 
but instead of operating on tables and columns its operates on JPA entities.

JPQL is used in JPA to create dynamic queries that can be executed agains relational database, these queries 
are defined as strings and executed using JPA EntityManager interface.

Example:
```java
String jpql = "SELECT e FROM Employee e WHERE e.department = :dept";

TypedQuery<Employee> query = entityManager.createQuery(jpql, Employee.class);
query.setParameter("dept", "IT");

List<Employee> results = query.getResultList();
```

## What are the advantages of using JPA over JDBC?
JPA is higher level abstraction of JDBC, some it's key advantages:
- **Object-relational mapping** It offers ORM framework that enables developers to map Java objects 
to database tables without having to create SQL queries, as result developers will have to write less code 
which is easier to maintain
- **Portability** Its standardized API that is independent of any specific database implementation
- **Transaction management** Simplifies process of managing database transactions 

## What is the difference between `JpaRepository`, `PagingAndSortingRepository` `CrudRepository`?
`JpaRepository` extends `PagingAndSortingRepository` which in turn extends `CrudRepository`

- `CrudRepository` provides CRUD functions
- `PagingAndSortingRepository` provides methods for sorting and pagination of records
- `JpaRepository` provides some JPA related methods such as flushing the persistence context and
deleting records in a batch.

## How to generate custom query method inside your repository?
You can generate method based on some rules and Spring will create these methods in proxy object in runtime
Example: `List<Person> findByEmailAddressAndLastname(EmailAddress emailAddress, String lastname);`
this technique called Derived Query Methods

Or if this functionality is not enough you can use `@Query("jpql or sql query")`, just put this annotation 
on top of the method, this annotation takes precedence over named queries, by default it expects JPQL.

Or you can create predefined query in your entity class using `@NamedQuery()` annotation 

## What is the purpose of `EntityManager` in JPA?
Entity manager in JPA is responsible for app interaction with persistance context which is responsible 
for managing the lifecycle of entity objects and their persistance in database. EntiyManager provides 
API for performing CRUD operations on the db using entity objects.

## What is the purpose of the `@JoinColumn` annotation in JPA?
The `@JoinColumn` used to specify a join column for relationship mapping between two entities. It is used
to define the columns in a table that will be used to establish association between two entities, where 
the one entity is the owner of the relationship(one that has the foreign key column) and the other side is 
the inverse side

## What types of cascades does JPA support?
- **CascadeType.ALL** cascades all operations
- **CascadeType.PERSIST** cascades persistent operation from the parent entity to the associated child 
entities
- **CascadeType.MERGE** cascades all merge operations from parent entity to all it's child entities
- **CascadeType.REMOVE** 
- **CascadeType.REFRESH**
- **CascadeType.DETACH**

And 3 more Hibernate extended types:
- **REPLICATE** 
- **SAVE_UPDATE**
- **LOCK**

## What is `FetchType`?
Parameter _fetch_ allows you to manage modes of loading dependent objects
- `FetchType.LAZY` - child elements are loaded only when they need in code
- `FetchType.EAGER` if we load parent data we also load all it's children data

## What do you know about n + 1 problem in JPA?
**N + 1** problem happens when hibernate executes N additional SQL statements to fetch 
the same data that could have been retrieved when executed the primary SQL query.

## How we can avoid or solve n + 1 problem?
If our we have related with our entity objects and use `FetchType.EAGER`(which is default for 
`@OneToOne` and for `@OneToMany`), then every time you request parent entity you'll have n additional queries.
To avoid this you should always use `JOIN FETCH` to get all the data via one request.

With `FetchType.LAZY` situation is better at first glance, but any time you'll request 
child entities of your parent object you'll get N additional queries, so you also need to use `JOIN FETCH`


## What is exception translation?
When you use Hibernate or any other JPA implementation in DAO you must decide how to handle persistence technology's
native exception classes. For catching such exceptions correctly you'll have to tie on the persistence technology, 
Spring provides exception translation to happen automatically through `@Repository` annotation. 

The postprocessor automatically looks for all exception translators and
(implementations of the `PersistanceExceptionTranslator`) and advises all beans marked with the `@Repository` so 
that discovered annotations can intercept and apply the appropriate translation on the thrown exceptions.


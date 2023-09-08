# JPA, Hibernate, Spring Data

## What is exception translation?
When you use Hibernate or any other JPA implementation in DAO you must decide how to handle persistence technology's
native exception classes. For catching such exceptions correctly you'll have to tie on the persistence technology, 
Spring provides exception translation to happen automatically through `@Repository` annotation. 

The postprocessor automatically looks for all exception translators and
(implementations of the `PersistanceExceptionTranslator`) and advises all beans marked with the `@Repository` so 
that discovered annotations can intercept and apply the appropriate translation on the thrown exceptions.


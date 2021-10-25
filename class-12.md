# Spring RequestMapping

## RequestMapping :

+ RequestMapping — by Path
+ RequestMapping — the HTTP Method 

### RequestMapping and HTTP Headers

+ @RequestMapping With the headers Attribute
+ @RequestMapping Consumes and Produces


### RequestMapping With Path Variables

+ Single @PathVariable
+ Multiple @PathVariable
+ PathVariable With Regex


# Accessing Data with JPA

+ Starting with Spring Initializr  : Download the resulting ZIP file

+ Define a Simple Entity :for example, you store Customer objects, each annotated as a JPA entity.

+ Create Simple Queries: 
Spring Data JPA focuses on using JPA to store data in a relational database. Its most compelling feature is the ability to create repository implementations automatically, at runtime, from a repository interface.

+ Create an Application Class:
Spring Initializr creates a simple class for the application.

+ Build an executable JAR :Building an executable jar makes it easy to ship, version, and deploy the service as an application throughout the development lifecycle, across different environments, and so forth.

## CrudRepository, JpaRepository, and PagingAndSortingRepository in Spring Data


+  Spring Data Repositories :

   + CrudRepository provides CRUD functions
   + PagingAndSortingRepository provides methods to do pagination and sort records
   + JpaRepository provides JPA related methods such as flushing the persistence context and delete records in a batch

+ PagingAndSortingRepository :
an interface, which extends CrudRepository:
This interface provides a method findAll(Pageable pageable), which is the key to implementing Pagination.

When using Pageable, we create a Pageable object with certain properties and we've to specify at least:

 + Page size
 + Current page number
 + Sorting 

 ex :
 
  public interface PagingAndSortingRepository<T, ID extends Serializable> 
  extends CrudRepository<T, ID> {

    Iterable<T> findAll(Sort sort);

    Page<T> findAll(Pageable pageable);
}
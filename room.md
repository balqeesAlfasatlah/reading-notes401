# Room

## Save data in a local database using Room 

+ common use case is to **cache relevant pieces of data** so that when the device cannot access the network, the user can still browse that content while they are offline.

+ The Room persistence library provides an abstraction layer over SQLite to allow fluent database access while harnessing the full power of SQLite.

+ **Room benefits:**

   1- Compile-time verification of SQL queries.

   2- Convenience annotations that minimize repetitive and error-prone boilerplate code.

   3- Streamlined database migration paths.

+ There are three major components in Room:

   1- The database class that holds the database and serves.

   2- Data entities that represent tables in your app's database.

   3- Data access objects (DAOs) that provide methods that your app can use to query, update, insert, and delete data in the database.


![](https://miro.medium.com/proxy/1*nPLp8XsB7e529f82XgddyA.png)


+ Defining data using Room entities :

  + you define entities to represent the objects that you want to store.
  
  + Each entity corresponds to a table in the associated Room database.

  + That means you can use Room entities to define your database schema without writing any SQL code.

  + Anatomy of an entity : You define each Room entity as a class that is annotated with @Entity.

  + Each Room entity must define a primary key

  + Define a composite primary key

+ Define relationships between objects :

  + Create embedded objects

  + **Define one-to-one relationships** :
    + where each instance of the parent entity corresponds to exactly one instance of the child entity.

    + create a class for each of your two entities. One of the entities must include a variable that is a reference to the primary key of the other entity.

    +  model the one-to-one relationship between the two entities.

  + **Define one-to-many relationships** :

    +  where each instance of the parent entity corresponds to zero or more instances of the child entity, but each instance of the child entity can only correspond to exactly one instance of the parent entity.

    + create a class for each of your two entities

    + model the one-to-many relationship between the two entities. 

  + **Define many-to-many relationships** :

    + where each instance of the parent entity corresponds to zero or more instances of the child entity.

    + create a class for each of your two entities.

    + model the relationship between the entities

## Accessing data using Room DAOs :

+ When you use the Room persistence library to store your app's data, you interact with the stored data by defining data access objects, or DAOs.

+  Each DAO includes methods that offer abstract access to your app's database.

+ By using DAOs to access your app's database you can preserve separation of concerns, a critical architectural principle.

+ Anatomy of a DAO : You can define each DAO as either an interface or an abstract class and you must always annotate your DAOs with @Dao.

+ There are two types of DAO methods that define database interactions:

  1- Convenience methods that let you insert, update, and delete rows in your database without writing any SQL code.

  2- Query methods that let you write your own SQL query to interact with the database.

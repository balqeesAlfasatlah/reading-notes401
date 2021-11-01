# Many to Many relationship

+ Many-to-many relationships define entities for which both side of the relationship can have multiple references to each other.

+ The Many-To-Many mapping represents a collection-valued association where any number of entities can be associated with a collection of other entities. In relational database any number of rows of one entity can be referred to any number of rows of another entity.

![](https://www.logicbig.com/tutorials/java-ee-tutorial/jpa/many-to-many/images/many-to-many.png)

+ For our example, we're going to model movies and superheroes. a movie can have multiple superheroes, and a superhero can appear in multiple movies. 


+ To model this many-to-many relationship using JPA, we will need three tables:

  1- MOVIE

  2- SUPER_HERO

  3- SUPERHERO_MOVIES


# Working with Relationships in Spring Data REST 

## One-to-One Relationship :

 here an example ER diagram for book database. to explain the relations :.

![](https://miro.medium.com/max/851/1*wAT6A6Cka5vKpTrm_rFzIw.png)

+ there is a **Many-to-Many relationship** between books and categories. A book can have more than one category, and a category can have more than one book. The same is true for the relationship between the book and the author.

+ Categories can have subcategories. These subcategories must be linked to a parent category. In this case, the **One-to-Many** relationship emerges.

+ There is also a photo table attached to the books. This table keeps the cover photos of the related book in different sizes. The relationship here will be **One-to-One**.

# Integration Testing in Spring
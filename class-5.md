# Big O

+ used to describe the efficiency of an algorithm or function. This efficiency is evaluated based on 2 factors:

1- Running Time (complexity) : the time a function needs to complete.

2- Memory Space (complexity) : the amount of memory resources a function uses to store data and instructions.

+ Big is to describe the **Worst Case** of efficiency.

+ 4 Key Areas for analysis:

  1- Input Size

  2- Units of Measurement

  3- Orders of Growth

  4- Best Case, Worst Case, and Average Case

---

# Linked Lists

+ Linked List : data structure that contains nodes that links/points to the next node in the list.

+ Node : are the individual items that live in a linked list and each node contains the data for each link.

+ There are two types of Linked List : 

  1- Singly : means that there is only one reference, and the reference points to the Next node in a linked list.

  2- Doubly : means that there is a reference to both the Next and Previous node.

  ![](https://fringster.com/content/images/16466.jpg)

  + **traversing** a linked list : we are not able to use a foreach or for loop. We depend on the **Next value** in each node to guide us where the next reference is pointing.

  ![](https://media.geeksforgeeks.org/wp-content/cdn-uploads/RGIF2.gif)


+ **Adding a Node** :

Order of operations important in Linked List , so you must be careful that all references to each link/node is properly assigned.

+ steps to add a new node : for example add  an O(1) efficiency.

![](https://image.slideserve.com/399223/inserting-a-node-into-a-specified-position-of-a-linked-list-n.jpg)

## Linear data structures :

![](https://media.geeksforgeeks.org/wp-content/uploads/20191010170332/Untitled-Diagram-183.png)

![](https://alldifferences.net/wp-content/uploads/2020/11/Difference-between-Linear-and-Non-Linear-Data-Structure.png)


+ Growing a linked list :

  1- First, we find the head node of the linked list.

  2- Next, we’ll make our new node, and set its pointer to the current first node of the list.

  3- Lastly, we rearrange our head node’s pointer to point at our new node.

 + **inserting an element at the end of a linked list :**

   1- Find the node we want to change the pointer of (in this case, the last node).

   2-Create the new node we want to insert and set its pointer (in this case, to null)

   3-Direct the preceding node’s pointer to our new node

   + the different between the arrays and linked list :

   ![](https://examradar.com/wp-content/uploads/2016/10/Comparison-between-array-and-linked-list.png)

![](https://i1.faceprep.in/Companies-1/difference-between-arrays-and-linked-list.png)
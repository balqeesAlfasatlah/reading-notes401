# RecyclerView

+ RecyclerView makes it easy to efficiently display large sets of data. 
+ You supply the data and define how each item looks
+ the RecyclerView library dynamically creates the elements when they're needed.


### Several different classes work together to build your dynamic list :

+ RecyclerView is the ViewGroup that contains the views corresponding to your data.

+ Each individual element in the list is defined by a view holder object. When the view holder is created, it doesn't have any data associated with it. After the view holder is created, the RecyclerView binds it to its data. 

+ The RecyclerView requests those views, and binds the views to their data, by calling methods in the adapter. 


+ The layout manager arranges the individual elements in your list. 

### Steps for implementing the RecyclerView :

1- First of all, decide what the list or grid is going to look like. 

2- Design how each element in the list is going to look and behave. extend the ViewHolder class. Your version of ViewHolder provides all the functionality for your list items. Your view holder is a wrapper around a View

3- Define the Adapter that associates your data with the ViewHolder views.

### Implementing the adapter and view holder :

+ determined the layout, then you need to implement your Adapter and ViewHolder. 

+ These two classes work together to define how your data is displayed. 

+ **The ViewHolder** is a wrapper around a View that contains the layout for an individual item in the list.

+ **The Adapter** creates ViewHolder objects as needed, and also sets the data for those views. 

+ The process of associating views to their data is called **binding**.


+ When you define your adapter, you need to override three key methods:

  1- onCreateViewHolder(): RecyclerView calls this method whenever it needs to create a new ViewHolder.

  2- onBindViewHolder(): RecyclerView calls this method to associate a ViewHolder with data. 

  3- getItemCount(): RecyclerView calls this method to get the size of the data set. 

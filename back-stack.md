# Tasks and the back stack 

**Task** is a collection of activities that users interact with when trying to do something in your app.

+ These activities are arranged in the back stack in the order in which each activity is opened. 


+ Lifecycle of a task and its back stack :

 When you start a new activity  that is (by default) pushing a new activity onto your task, causing the previous Activity to be paused or stopped if the new activity fully obscures the previous activity.


![](https://i.stack.imgur.com/UqCiz.png)


## Save key-value data

+ we use the **SharedPreferences** APIs to store and retrieve simple values.

+ **SharedPreferences object** points to a file containing key-value pairs and provides simple methods to read and write them.

+ Each SharedPreferences file is managed by the framework and can be private or shared. 

1- create a new shared preference by calling one of these methods:

  + **getSharedPreferences()** :  Use this if you need multiple shared preference files identified by name, which you specify with the first parameter.

  + **getPreferences()** : Use this from an Activity if you need to use only one shared preference file for the activity. 
  

2- Write to shared preferences :

   + create a **SharedPreferences.Editor** by calling edit() on your SharedPreferences.

   + Pass the keys and values you want to write with methods such as putInt() and putString(). Then call apply() or commit() to save the changes.

3- Read from shared preferences :'

  + To retrieve values from a shared preferences file, call methods such as getInt() and getString(), providing the key for the value you want.
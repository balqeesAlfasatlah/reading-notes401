# Android Fundamentals

### Each Android app lives in its own security sandbox, protected by the following Android security features:


+ he Android operating system is a multi-user Linux system in which each app is a different user.

+ By default, the system assigns each app a unique Linux user ID (the ID is used only by the system and is unknown to the app). 

+ Each process has its own virtual machine (VM), so an app's code runs in isolation from other apps.

+ By default, every app runs in its own Linux process. The Android system starts the process when any of the app's components need to be executed, and then shuts down the process when it's no longer needed or when the system must recover memory for other apps.

## App components :

**1- Activities :**
It represents a single screen with a user interface the activity has essentially four states:

+ If an activity is in the foreground of the screen (at the highest position of the topmost stack), it is active or running.

+ If an activity has lost focus but is still presented to the user, it is visible.

+ If an activity is completely obscured by another activity, it is stopped or hidden.

+ The system can drop the activity from memory by either asking it to finish, or simply killing its process, making it destroyed


![](https://developer.android.com/images/activity_lifecycle.png)


**2- Services :** is a general-purpose entry point for keeping an app running in the background for all kinds of reasons and it does not provide a user interface.

 **example** : a service might play music in the background while the user is in a different app.

 + There are two types of services that tell the system how to manage an app :

   + Started services : tell the system to keep them running until their work is completed.

   + Bound services : run because some other app (or the system) has said that it wants to make use of the service. This is basically the service providing an API to another process. 

**3- Broadcast receivers :** a component that enables the system to deliver events to the app outside of a regular user flow, 

**4- Content providers :** manages a shared set of app data that you can store in the file system

## Activating components :

+ Three of the four component types—activities, services, and broadcast receivers—are activated by an asynchronous message called an **intent**.

+ **Intents** bind individual components to each other at runtime.


+ An intent is created with an Intent object, which defines a message to activate either a specific component (**explicit intent**) or a specific type of component (**implicit intent**).

## The manifest file :

The system must know that the component exists by reading the app's manifest file , the app must declare all its components in this file.

+ You must declare all app components using the following elements:

   + <"activity"> elements for activities.
   + <"service"> elements for services.
   + <"receiver"> elements for broadcast receivers.
   + <"provider"> elements for content providers.
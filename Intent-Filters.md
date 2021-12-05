# Intent Filters

+ Allowing Other Apps to Start Your Activity ,
If your app can perform an action that might be useful from another app, your app should be prepared to respond to action requests by specifying the appropriate intent filter in your activity.

+ To allow other apps to start your activity in this way, you need to add an <intent-filter> element in your manifest file for the corresponding <activity> element.

+ When your app is installed on a device, the system identifies your intent filters and adds the information to an internal catalog of intents supported by all installed apps. 

+ When an app calls startActivity() or startActivityForResult(), with an implicit intent, the system finds which activity (or activities) can respond to the intent.

## Add an Intent Filter

+ In order to properly define which intents your activity can handle, each intent filter you add should be as specific as possible in terms of the type of action and data the activity accepts.

+ The system may send a given Intent to an activity if that activity has an intent filter fulfills the following criteria of the Intent object:

**Action**

+ A string naming the action to perform.

+  Usually one of the platform-defined values such as ACTION_SEND or ACTION_VIEW.

+ Specify this in your intent filter with the <action> element.

+ The value you specify in this element must be the full string name for the action, instead of the API constant (see the examples below).

**Data**

+ A description of the data associated with the intent.

+ Specify this in your intent filter with the <data> element.

+ Using one or more attributes in this element, you can specify just the MIME type, just a URI prefix, just a URI scheme, or a combination of these and others that indicate the data type accepted.


**Category**

+ Provides an additional way to characterize the activity handling the intent, usually related to the user gesture or location from which it's started. 

+ There are several different categories supported by the system, but most are rarely used.

+ However, all implicit intents are defined with CATEGORY_DEFAULT by default.
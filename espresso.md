# Espresso

+ Testing user interactions within a single app helps to ensure that users do not encounter unexpected results or have a poor experience when interacting with your app.

+ Use Espresso to write concise, beautiful, and reliable Android UI tests.

+ **Target audience**

  Espresso is targeted at developers, who believe that automated testing is an integral part of the development lifecycle. 


## Create UI tests with Espresso Test Recorder 

+ **Espresso Test Recorder :** tool lets you create UI tests for your app without writing any test code.

+ By recording a test scenario, you can record your interactions with a device and add assertions to verify UI elements in particular snapshots of your app.

+  Espresso Test Recorder then takes the saved recording and automatically generates a corresponding UI test that you can run to test your app.

+ **Record UI interactions**

  To start recording a test with Espresso Test Recorder, proceed as follows:

    1- Click Run > Record Espresso Test
    
    2- In the Select Deployment Target window, choose the device on which you want to record the test. 

    3- Espresso Test Recorder triggers a build of your project, and the app must install and launch before Espresso Test Recorder allows you to interact with it. 

+ Recorded interactions will appear in the main panel in the Record Your Test window.


### **Add assertions to verify UI elements :**


+ Assertions verify the existence or contents of a View element through three main types:

  1- text is: Checks the text content of the selected View element

  2- exists: Checks that the View element is present in the current View hierarchy visible on the screen

  3- does not exist: Checks that the View element is not present in the current View hierarchy


 ## Save a recording :

+ use the following steps to save your recording and generate the Espresso test:

    1- Click Complete Recording. The Pick a test class name for your test window appears.

    2- Espresso Test Recorder gives your test a unique name within its package. Use the Test class name text field if you want to change the suggested name. Click Save.

   3- The file automatically opens after Espresso Test Recorder generates it, and Android Studio shows the test class as selected in the Project window of the IDE.
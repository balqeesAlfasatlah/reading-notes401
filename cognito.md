# Cognito

+ The Amplify Auth category provides an interface for authenticating a user.

+ Behind the scenes, it provides the necessary authorization to the other Amplify categories. It comes with default, built-in support for Amazon Cognito User Pool and Identity Pool. 

+ The Amplify CLI helps you to create and configure the auth category with an authentication provider.

+ **Goal :**

  To setup and configure your application with Amplify Auth and go through a simple api to check the current auth session

## Configure Auth Category :

1- amplify add auth

2- amplify push

3-Install Amplify Libraries :

 dependencies {
    implementation 'com.amplifyframework:aws-auth-cognito:1.30.0'
}

4-Initialize Amplify Auth

 // Add this line, to include the Auth plugin.
RxAmplify.addPlugin(new AWSCognitoAuthPlugin());
RxAmplify.configure(getApplicationContext());

5- Check the current auth session

+ **Sign in :**

  The Auth category can be used to register a user, confirm attributes like email/phone, and sign in with optional multi-factor authentication. It is set up to use Amazon Cognito User Pools which manages the users and their properties.
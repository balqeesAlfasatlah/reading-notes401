#  Serverless Architecture

+ **Serverless :** is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers.

+  A serverless application runs in stateless compute containers that are event-triggered, ephemeral (may last for one invocation), and fully managed by the cloud provider. 

+ Most of the cloud providers have invested heavily in serverless and thats a lot of money .

  Here are some of the currently available cloud services:


 + AWS Lambda , Google Cloud Functions , Azure Functions , 
 Azure Functions , IBM OpenWhisk , Alibaba Function Compute

 + **Pricing** : one of the major advantages of using Serverless is reduced cost

 + **Networking :**
The downside is that Serverless functions are accessed only as private APIs. To access these you must set up an API Gateway. This doesn’t have an impact on your pricing or process, but it means you cannot directly access them through the usual IP


+ **Functions as a Service (FaaS)**

    FaaS is an implementation of Serverless architectures where engineers can deploy an individual function or a piece of business logic. They start within milliseconds  and process individual requests within a 300-second timeout imposed by most cloud vendors.

    + Principles of FaaS:

        - Complete management of servers
        - Invocation based billing
        - Event-driven and instantaneously scalable


 + Benefits of Serverless Architecture
  
   + From business perspective :

        + The cost incurred by a serverless application is based on the number of function executions, measured in milliseconds instead of hours.

        + Process agility

        + Cost of hiring backend infrastructure engineers goes down.

        + Reduced operational costs

    + From developer perspective :

        + Reduced liability, no backend infrastructure to be responsible for.

        + Zero system administration.

        + Easier operational management.

        + Fosters adoption of Nanoservices, Microservices, SOA Principles.

        + Faster set up.
       
+ From user perspective :

    + If businesses are using that competitive edge to ship features faster, then customers are receiving new features quicker than before.

    + It is possible that users can more easily provide their own storage backend(i.e Dropbox, Google Drive).

    + It’s more likely that these kinds of apps may offer client-side caching, which provides a better offline experience.       


## AWS Amplify

**AWS Amplify** is a set of purpose-built tools and services that makes it quick and easy for front-end web and mobile developers build full-stack applications on AWS, with the flexibility to leverage the breadth of AWS services to further customize applications. 

+ Amplify supports popular languages, frameworks, and platforms

+ Use cases :

  + Create onboarding flows
  + Collaborate in real time
  + Unlock AI/ML capabilities
  + Launch targeted campaigns

### API (GRAPHQL)

+ The GraphQL Transform provides a simple to use abstraction that helps you quickly create backends for your web and mobile applications on AWS.

+ The GraphQL Transform simplifies the process of developing, deploying, and maintaining GraphQL APIs. 

+ Create a GraphQL API :

  + Navigate into the root of a JavaScript, iOS, or Android project and run:

 + amplify init
  Follow the wizard to create a new app. After finishing the wizard run:

+ amplify add api
 
  Select the following options:

+ Select GraphQL
When asked if you have a schema, say No
Select one of the default samples; you can change this later
Choose to edit the schema and it will open the new schema.graphql in your editor
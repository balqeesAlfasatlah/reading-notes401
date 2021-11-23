## Serverless

+ **Serverless :** is a cloud computing execution model where the cloud provider dynamically manages the allocation and provisioning of servers.

+  A serverless application runs in stateless compute containers that are event-triggered, ephemeral (may last for one invocation), and fully managed by the cloud provider. 

+ Most of the cloud providers have invested heavily in serverless and thats a lot of money .

## Amplify

**AWS Amplify** is a set of purpose-built tools and services that makes it quick and easy for front-end web and mobile developers build full-stack applications on AWS, with the flexibility to leverage the breadth of AWS services to further customize applications. 

+ Amplify supports popular languages, frameworks, and platforms

# GraphQL @connection

+ The Amplify CLI provides GraphQL directives to enhance your schema with additional capabilities .

+ Amplify-provided directives :

    + @model: Defines top level object types in your API that are backed by Amazon DynamoDB

     + @key: Configures custom index structures for @model types

     + @auth: Defines authorization rules for your @model types and fields

    + @connection: Defines 1:1, 1:M, and N:M relationships between @model types

    + @function: Configures a Lambda function resolvers for a field
  

+ AWS AppSync-provided directives :

The following directives are supported by the AppSync service and can be used within the Amplify GraphQL schemas.

+  These will not be processed by Amplify CLI but passed through to the service as is and will be present in the output schema. 

+ For example, Amplify's @auth directive will add these directives under the hood to the output schema.

    + @aws_api_key
    + @aws_iam
    + @aws_oidc
    + @aws_cognito_user_pools
    + @aws_auth
    + @aws_subscribe
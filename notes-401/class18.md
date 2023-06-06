# AWS: API, Dynamo and Lambda

## [AWS API Gateway Overview](https://www.serverless.com/amazon-api-gateway)

1. What is Amazon API Gateway?

Amazon API Gateway is a fully managed service that makes it easy for developers to create, publish, maintain, monitor, and secure APIs at any scale. It acts as a "front door" for applications to access data, business logic, or functionality from your backend services.

2. Why is Amazon API Gateway an important part of the Serverless ecosystem?

In the Serverless ecosystem, API Gateway plays a crucial role by providing a point of entry that routes requests to the appropriate backend service, typically a function in AWS Lambda. This allows developers to focus on writing their application code, without worrying about managing and operating servers, as API Gateway handles all the tasks involved in accepting and processing concurrent API calls.

3. How does API Gateway integrate with other AWS services?

API Gateway integrates with many AWS services. For example, it can trigger AWS Lambda functions, send traffic to a publicly accessible endpoint, or access multiple AWS services like Amazon DynamoDB, AWS Step Functions, or Amazon SQS. It can also be integrated with Amazon Cognito for user authentication and authorization.

## [AWS API Gateway](https://aws.amazon.com/api-gateway/)

1. What are the some benefits of using Amazon API Gateway?

Efficient API development: It streamlines the process of deploying and managing APIs.
Scalability: It can handle any amount of traffic received by an API.
Flexibility: It supports RESTful APIs and WebSocket APIs.
Security: It supports AWS Identity and Access Management (IAM) roles, Cognito User Pools, and Lambda authorizers for user authorization.
Cost-effective: With its pay-as-you-go model, you only pay for the API calls you receive and the amount of data transferred.

2. What two API types might you choose from?

Amazon API Gateway provides support for two types of APIs: RESTful APIs and WebSocket APIs.


## [AWS DynamoDB Guide](https://www.dynamodbguide.com/what-is-dynamo-db/)

1. What is DynamoDB?

Amazon DynamoDB is a key-value and document database that provides single-digit millisecond performance at any scale. It's a fully managed, multiregion, multimaster database with built-in security, backup and restore, and in-memory caching for internet-scale applications.

2. Under what circumstances would you recommend DynamoDB over MongoDB?

DynamoDB would be a good choice when you need a fully managed service that provides seamless scalability, high performance, and integration with other AWS services. It's also preferable when predictable performance, high availability, and automatic replication across multiple regions are critical.

## [AWS DynamoDB](https://aws.amazon.com/dynamodb/)

1. Explain to a non-technical friend how DynamoDB works.

Imagine you have a massive filing system with billions of files. If you had to find a specific file, it would take you a long time to search through them all. DynamoDB is like an incredibly efficient filing system. It organizes and stores your files (or data, in this case) in a way that allows you to find exactly what you're looking for almost instantly, no matter how much data you have.

## [Dynamoose](https://dynamoosejs.com/getting_started/Introduction)

1. What is Dynamoose?

Dynamoose is a modeling tool for Amazon's DynamoDB, inspired by Mongoose, which is a MongoDB object modeling tool. Dynamoose makes it easy to interact with DynamoDB by providing a set of APIs and a structure to your data.

2. What are some key features of Dynamoose?

- Schema: Just like Mongoose for MongoDB, Dynamoose allows you to define a schema for your data. This schema helps enforce data structure and types, which can be especially useful in JavaScript environments.

- Model: Dynamoose allows you to create models based on your schema, which can then be used to interact with your DynamoDB database. This includes operations like creating, reading, updating, and deleting records.

- Ease of Use: Dynamoose abstracts away much of the complexity of DynamoDB, providing a simple API for interacting with your database. This makes it more straightforward to perform common tasks.

- Chainable API: Dynamoose provides a chainable API for querying your database, making it easy to build up complex queries.

- Plugin System: Dynamoose supports plugins, which allow you to extend its functionality to suit your specific needs.

- Pre and Post Hooks: Much like Mongoose, Dynamoose supports pre and post hooks (also known as middleware), which allow you to run custom code before or after certain operations. For example, you could use a pre-hook to validate or modify data before it's saved to the database.


## Reflection
- What are your learning goals after reading and reviewing the class README?
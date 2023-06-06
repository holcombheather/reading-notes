# AWS: Events

## [AWS SQS vs SNS](https://medium.com/awesome-cloud/aws-difference-between-sqs-and-sns-61a397bf76c5)

1. What is the difference betweeen SQS and SNS?

  Amazon SQS (Simple Queue Service) and SNS (Simple Notification Service) are both messaging services within AWS, but they're used for different purposes.

  SQS is a distributed message queuing service. It's used for decoupling point-to-point communication between services, components, or devices. It enables the sending, storing, and receiving of messages at any volume, without losing messages or requiring other services to be available.

  SNS, on the other hand, is a fully managed pub/sub (publish/subscribe) messaging service. It enables the sending of individual messages to multiple subscribers, all of whom receive identical copies of the message. Subscribers can be services, email addresses, mobile devices (for push notifications), or HTTP/HTTPS endpoints.

2. What are some use cases for both SNS and SQS?

  SNS is used in cases where you want to send the same message to multiple subscribers. This is often used for microservices architecture communication, email, or SMS notification systems, or distributing data to many recipients for parallel processing.

  SQS is used when you need to ensure a series of tasks are completed in order or when you want to distribute tasks among different workers. Use cases include decoupling application components, batch tasks processing, or delaying tasks for future execution.

## [AWS SNS and SQS](https://www.youtube.com/watch?v=mXk0MNjlO7A)

1. Describe how to use SQS and SNS in a “fanout” pattern.

  The "fanout" pattern involves a single message being delivered to multiple endpoints. In AWS, you can use SNS in conjunction with SQS to accomplish this.

  You start by creating an SNS Topic. You then create multiple SQS queues and subscribe each of them to the SNS Topic. When a message is published to the SNS Topic, it gets delivered to all the SQS queues that are subscribed to the Topic. Each SQS queue can then be processed independently, allowing for parallel processing and redundancy.

2. Explain how “push notifications” work, using SNS.

  Push notifications with SNS work by sending a message to an SNS Topic, which has been configured to send notifications to a specific endpoint. This endpoint could be a mobile device, a Lambda function, an SQS queue, or other supported AWS services.

  When the message is published to the Topic, SNS pushes the message to all the subscribers, which could be multiple endpoints. In the case of mobile push notifications, the message gets sent to a push notification service (like APNS for iOS or FCM for Android), which then sends the notification to the user's device.


## [SQS and SNS Basics](https://www.youtube.com/watch?v=UesxWuZMZqI)

1. How might a large scale, distributed application make use of a Queue system like SQS?

  Large scale, distributed applications often have components that need to communicate with each other, but you don't want these components to be tightly coupled. Using SQS, these components can communicate asynchronously by sending messages to a queue.

  This enables several benefits. First, it helps to decouple your application components, allowing them to run and scale independently. Second, it provides a buffer if there are spikes in traffic, as the queue can hold the messages until the consuming component is ready to process them. Third, it ensures that messages aren't lost if a component fails, as the message stays in the queue until it's successfully processed.

## Quick Links

- [SNS Javascript SDK](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SNS.html)

- [SQS Javascript SDK](https://docs.aws.amazon.com/AWSJavaScriptSDK/latest/AWS/SQS.html)

### Reflection
- What are your learning goals after reading and reviewing the class [README](https://codefellows.github.io/code-401-javascript-guide/curriculum/class-19/)?
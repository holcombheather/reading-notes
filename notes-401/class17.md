# AWS: S3 and Lambda

## [AWS S3](https://aws.amazon.com/s3/)

1. What is Amazon S3?

  Amazon S3 (Simple Storage Service) is a scalable, high-speed, web-based cloud storage service designed for online backup and archiving of data and applications on Amazon Web Services (AWS). It allows you to store and retrieve any amount of data, at any time, from anywhere on the web.

2. Name some use cases for Amazon S3.

  Backup and Restore: S3 can be used for backing up critical data, applications, and databases to recover them in case of a disaster.
  Data Archiving: S3 can be used for long-term cold storage of data that is accessed infrequently.
  Website Hosting: Static websites can be hosted on S3, making it an affordable and scalable solution for website hosting.
  Data Lake: S3 can be used as a Data Lake, storing vast amounts of raw data in its native format until it is needed.

3. Name some benefits of using Amazon S3.

  - Durability and Availability: S3 offers 99.999999999% (11 9's) durability and 99.99% availability of objects over a given year.
  - Scalability: S3 can store any amount of data and scale up as your needs grow.
  - Security: S3 provides advanced security features such as encryption and access control to keep your data secure.
  - Integration with Other AWS Services: S3 integrates well with other AWS services like EC2, Lambda, and CloudWatch, making it a versatile choice for various applications.

## [AWS Lambda Basics](https://www.serverless.com/aws-lambda)

1. What is AWS Lambda?

  AWS Lambda is a serverless compute service that runs your code in response to events and automatically manages the underlying compute resources for you. You can use AWS Lambda to extend other AWS services with custom logic, or create your own back-end services that operate at AWS scale, performance, and security.

2. Name some use cases for AWS Lambdas.

  - Real-Time File Processing: Lambda can be used to process files as soon as they are uploaded to Amazon S3 (e.g., for data transformation, resizing images).
  - Data Transformation: Lambda can be used for cleaning and transforming data for analytics.
  - Real-Time Stream Processing: Lambda can process real-time streams of data (e.g., for application activity tracking, transaction order processing).
  - Serverless Backend: Lambda can power your application’s backend that operates at AWS scale, performance, and security.

3. Describe “serverless” to a non-technical friend.

  Imagine if you had a light bulb in your home, but you didn't have to worry about the electricity powering it. You could just turn the light on and off as you wish, and only pay for the amount of light you use. You wouldn't have to think about the power station generating the electricity or the cables bringing it to your house. This is like serverless computing. When you want to run a program or use an application on the internet, you don't need to worry about the servers (the computers) that power it. They're there, behind the scenes, but you just use the service you need and pay for what you use, without managing any of the underlying infrastructure.


## [CDN](https://cyberhoot.com/cybrary/content-delivery-network-cdn/)

1. What is a CDN?

  A Content Delivery Network (CDN) is a system of distributed servers that deliver web content to a user based on their geographic location, the origin of the web page and a content delivery server. It is used to distribute the load of delivering content, often to optimize for speed and performance.

2. How does a CDN work with relation to the website visitor?

  When a user requests content (like a webpage or a video), that request doesn't go straight to the site's main server. Instead, it's redirected to a CDN edge server that's closer in terms of network hops. Because the content is stored on a CDN, it's closer to the user, so it arrives faster than it would if it had to be delivered from the site's central server.

3. What are the benefits of employing a CDN?

  - Performance: CDN improves website load times by serving content from the nodes closest to the website visitors.
  - Scalability: CDNs are designed to absorb sudden traffic spikes and heavy loads, like during major events or peak shopping times.
  - Security: CDNs can provide improved security measures, including protection against DDoS attacks.
  - Reduced Bandwidth Costs: By caching content and serving it to users, CDNs can significantly cut down on data costs from your primary hosting provider.
  - Increased content availability and redundancy: CDNs can handle more traffic and withstand hardware failure better than many origin servers.
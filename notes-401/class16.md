# AWS: Cloud Servers


## [AWS EC2](https://aws.amazon.com/ec2/)

1. What is an EC2 Instance?

  An Amazon EC2 instance is a virtual server in Amazon's Elastic Compute Cloud (EC2) for running applications on the Amazon Web Services (AWS) infrastructure. It provides scalable computing capacity in the cloud and enables developers to launch and manage server instances with a variety of operating systems.

2. Name 2 use cases for EC2.

  - **Web Hosting**: EC2 instances can be used for scalable web hosting. Websites hosted on EC2 can easily scale up or down based on the traffic, making it efficient for handling unexpected traffic spikes.
  - **Data Processing**: EC2 instances can be used for large scale data processing using Hadoop, Spark or other big data processing tools. It provides the ability to process large data sets on a cluster of servers.

3. Provide 1 reason to use ECS instead of a service such as Heroku, Digital Ocean, or Render.com.

  Scalability and control: AWS ECS (Elastic Container Service) provides deeper control and allows you to finely tune the underlying infrastructure. It allows you to choose the EC2 instance types best suited for your application, and you can adjust and scale your resources as needed. This level of control is often not available in platform-as-a-service (PaaS) offerings like Heroku or other cloud providers like Digital Ocean and Render.com, which may have more restrictions or predefined settings.


## [EC2 For Humans](https://www.youtube.com/watch?v=lZMkgOMYYIg)

1. Where can we find EC2 on the AWS Console?

  After logging into your AWS Management Console, you can find EC2 by typing "EC2" into the service search bar or by finding it under the "Compute" category in the All Services section.

2. Explain the general difference between T2 Micro and XL.

  T2 Micro and XL are different types of EC2 instances, each with different levels of computational power, memory, and storage:

  - T2 Micro: This is the smallest and cheapest T2 instance type. It comes with 1 vCPU and 1 GiB of memory. It's a good choice for low-traffic web servers, developer environments, and small databases.
  - XL Instance: An "XL" (extra large) instance type provides more computational power and memory than the T2 Micro. The exact specifications depend on the specific XL instance family. These instance types are typically used for resource-heavy applications like large databases and high-traffic web servers.

3. Explain a “Compute Cycle” to a non-technical friend.

  A "compute cycle" can be thought of as a unit of work a computer can do, like a basic calculation or operation. Just like a car uses a cycle of its engine to move a certain distance, a computer uses a compute cycle to do a piece of work. When you use a service like EC2, you're essentially renting a certain number of these compute cycles to run your programs or applications.

## [Elastic Beanstalk](https://www.youtube.com/watch?v=SrwxAScdyT0)

1. What is Elastic Beanstalk?

  AWS Elastic Beanstalk is a service offered by Amazon for deploying and scaling applications developed with Java, .NET, PHP, Node.js, Python, Ruby, Go, and Docker on familiar servers such as Apache, Nginx, Passenger, and IIS. It reduces management complexity without restricting choice or control. You simply upload your application, and Elastic Beanstalk automatically handles the details of capacity provisioning, load balancing, scaling, and application health monitoring.

2. Describe the relationship between EC2 and Elastic Beanstalk.

  Amazon EC2 and Elastic Beanstalk are both part of Amazon Web Services. EC2 provides the raw computing resources, like servers, that your applications run on. Elastic Beanstalk, on the other hand, is a service that uses EC2 instances to simplify the deployment and scalability of your applications.

  When you deploy an application on Elastic Beanstalk, it automatically provisions and configures the resources you need, which includes EC2 instances. Therefore, Elastic Beanstalk is built on top of EC2 and uses EC2 instances to run your application.

3. Name some benefits of using Elastic Beanstalk.

  - **Automated operations**: Elastic Beanstalk automates various tasks like provisioning of resources, load balancing, automatic scaling, and application health monitoring, which allows developers to focus more on their application.

  - **Easy to start**: With Elastic Beanstalk, you just need to upload your application code and the service handles all the deployment details.

  - **Managed environment**: Elastic Beanstalk provides a managed environment which is a big advantage for developers who prefer not to manually handle the underlying infrastructure.

  - **Resource control**: Even though Elastic Beanstalk is a managed service, it still allows developers to have full control over the AWS resources that are created for running the application.

  - **Integrated with other AWS services**: Elastic Beanstalk is integrated with several AWS services like S3, RDS, and CloudWatch which can be used alongside it for improved functionality.

Quick Links

- [Virtual Machines](https://www.youtube.com/watch?v=yIVXjl4SwVo)
- [VMS and the Cloud](https://www.youtube.com/watch?v=l0DfHUWMjsU)
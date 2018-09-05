## AWS

### CI / CD

- [Practicing Continuous Integration and Continuous Delivery on AWS](https://d1.awsstatic.com/whitepapers/DevOps/practicing-continuous-integration-continuous-delivery-on-AWS.pdf)

### Developer Associate Exam

- [S3 FAQ](https://aws.amazon.com/s3/faqs/)
- [AWS Certified Developer Associate Exam Guide](https://d1.awsstatic.com/training-and-certification/docs-dev-associate/AWS_Certified_Developer_Associate_Updated_June_2018_Exam_Guide_v1.3.pdf)
- [Udemy Course - AWS Certified Developer - Associate 2018](https://www.udemy.com/aws-certified-developer-associate/)
- [AWS Certified Developer - Associate Level Exam Blueprint](http://awstrainingandcertification.s3.amazonaws.com/production/AWS_certified_developer_associate_blueprint.pdf)
- [AWS Certified Developer – Associate Level Sample Exam Questions 1](http://d0.awsstatic.com/training-and-certification/docs/AWS_certified_developer_associate_examsample.pdf)
- [AWS Certified Developer – Associate Level Sample Exam Questions 2](https://d1.awsstatic.com/training-and-certification/docs-dev-associate/AWS_certified_developer_associate_examsample.pdf)
- [Resources - acloud.guru](https://acloud.guru/)

#### Sample questions

- Your application is trying to upload a 6 GB file to Simple Storage Service and receive a "Your proposed upload exceeds the maximum allowed object size." error message. Use the multipart upload API for this object.
- EC2 instances are launched from Amazon Machine Images (AMIs). Can only be used to launch EC2 instances in the same AWS region as the AMI is stored.
- You have an EBS root device on /dev/sda1 on one of your EC2 instances. You are having trouble with this particular instance and you want to either Stop/Start, Reboot or Terminate the instance but you do NOT want to lose any data that you have stored on /dev/sda1. Hence you are unsure as to what would be best and if you will lose this data using any of these methods to change your instance state. Which of the below statements best describes the effect each change of instance state would have on the data you have stored on /dev/sda1? The data in an instance store is not permanent - it persists only during the lifetime of the instance. The data will be lost if you terminate the instance, however the data will remain on /dev/sda1 if you reboot or stop/start the instance because data on an EBS volume is not ephemeral.
- Which API call would best be used to describe an Amazon Machine Image? DescribeImages.
- Someone on your team configured a Virtual Private Cloud with two public subnets in two separate AZs and two private subnets in two separate AZs. Each public subnet AZ has a matching private subnet AZ. The VPC and its subnets are properly configured. You also notice that there are multiple webserver instances in the private subnet, and you've been charged with setting up a public-facing Elastic Load Balancer which will accept requests from clients and distribute those requests to the webserver instances. How can you set this up? Select both of the public subnets when configuring the ELB.
- Describe the process of registering a mobile device with SNS push notification service using GCM. Submit GCM notification credentials to Amazon SNS, then receive the Registration ID for each mobile device. After that, pass the device token to SNS, and SNS then creates a mobile subscription endpoint for each device and communicates with the GCM service on your behalf.
- Regarding the evaluation logic when managing Access to Your Amazon SNS Topics, the following things can be stated.The goal at evaluation time is to decide whether a given request should be allowed or denied. The evaluation logic follows several basic rules:- By default, all requests to use your resource coming from anyone but you are denied- An allow overrides any default denies- An explicit deny overrides any allows- The order in which the policies are evaluated is not important- A policy results in a default deny if it doesn't directly apply to the request.Keeping the above in mind, what will be the policy result, if a user requests to use Amazon SNS, but the policy on the topic doesn't refer to the user's AWS account at all? An explicit deny.
- Which of the following would you not expect to see in an SNS message body? SubjectId
- Which of the following would you expect to see in the body of an SNS notification? UnsubscribeURL
- You have just set up a push notification service to send a message to an app installed on a device with the Apple Push Notification Service. It seems to work fine. You now want to send a message to an app installed on devices for multiple platforms, those being the Apple Push Notification Service(APNS) and Google Cloud Messaging for Android (GCM). What do you need to do first for this to be successful? Get a set of credentials in order to be able to connect to the push notification service you are trying to setup.
- Amazon Simple Notification Service (Amazon SNS) provides support for delivery of message attributes to Amazon SQS endpoints and each message attribute consists of the following items: Name, Type and Value. Which of the following is TRUE, regarding message attributes? Name, type, and value must not be empty or null and the message body shouldn't be empty or null either.
- Which of the following is not a benefit of a query over a scan? It does not do consistent reads.
- What is the key feature of SWF? Guarantees delivery order of messages/tasks.
- What is the maximum number of S3 buckets by default allowed per AWS account? 100
- What is the maximum number of SWF domains allowed in an AWS account? 100
- In DynamoDB, how many tables can an AWS account have per region? 256
- For how long can a SWF workflow task or task execution can live up to? 1 year
- How many secondary indexes are allowed per table? 5
- Which of the following datatypes can be indexed in DynamoDB. String / Number / Boolean
- What is maximum limit for the size of an item collection in DynamoDB? 10GB
- What is the smallest amount of reserved capacity that can be purchased for DynamoDB? 100
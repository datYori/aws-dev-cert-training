# My AWS Dev cert path


## New to AWS and/or Cloud computing


- [X]  [Job roles in the cloud](https://www.aws.training/Details/eLearning?id=11987)
- [X] [AWS Cloud Practitioner Essentials](https://www.aws.training/Details/eLearning?id=60697)


> Personal key outcomes 
>  - 1 region = at least 2 AZ 
>  - Security Groups (VPC context) = stateful and deny and deny all inboud by default
>  - Storage capacity of snowball edge optimized : 80TB
>  - build, train, and deploy ML models : Amazon sage Maker    
>  - capacity storage AWS Snowmobile : 100PB


## Containers

### Amazon ECS

- [x] Amazon ECS 
  - <a href="http://www.youtube.com/watch?feature=player_embedded&v=qbEPae8YNbs
    " target="_blank"><img src="http://img.youtube.com/vi/qbEPae8YNbs/0.jpg" 
    alt="Deep Dive on Amazon Amazon Elastic Container Service (Amazon ECS) youtube video" width="240" height="180" border="10" /></a>

  > Personal key outcomes :
    > - [awslabs/ecs-refarch-continuous-deployment](https://github.com/awslabs/ecs-refarch-continuous-deployment)
    > - [awslabs/ecs-refarch-cloudformation](https://github.com/awslabs/ecs-refarch-cloudformation)
    > - [twitt collector](https://github.com/PaulMaddox/rpc-demo)
    > - [more on ECS](https://github.com/nathanpeck/awesome-ecs)

  - [ ] [AWS ECS Workshops](https://ecsworkshop.com/)



### Amazon EKS

- [x] [Amazon Elastic Kubernetes Service (EKS) Primer](https://www.aws.training/Details/eLearning?id=32894)


## Serverless

### New to serverless

- [x] [Introduction to Serverless Development](https://www.aws.training/Details/eLearning?id=27074)
- [x] [Getting into the Serverless Mindset](https://www.aws.training/Details/eLearning?id=27198)

### AWS Lambda

- [x] [AWS Lambda Foundations](https://www.aws.training/Details/eLearning?id=27197)


### Various serverless perspectives with AWS services

- [x] [Amazon API Gateway for Serverless Applications](https://www.aws.training/Details/eLearning?id=27199)
- [x] [Amazon DynamoDB for Serverless Architectures](https://www.aws.training/Details/eLearning?id=27196)
    > Personal key outcomes 
    > - basic factor for success with DynamoDB = choosing high cardinality partition key for even item  and request distribution
    > - Local secondary indexes can only be defined at the time of base table creation – they cannot be deleted without deleting the base table
    > - When you set an attribute for use by TTL, the value you should set for that attribute to result in expiry = epoch timestamp(with unit seconds) after which item can be deleted
    > - Optimistic concurrency control in DynamoDB = Read, transform, conditionally write, retry as required
    > - parameters to DynamoDB Auto Scaling = Min capacity, Max cap, Target utilization
- [ ] [CI/CD for serverless applications](https://cicd.serverlessworkshops.io/)
- [ ] [AWS Alien Attack: A Serverless Adventure](https://alienattack.workshop.aws/)

## Infrastructure as Code

- [x] [AWS Cloud dev kit (Workshop)](https://cdkworkshop.com/)

## AWS Developper Tools (if you are giga new to DevOps concepts)

- [x] [Introduction to AWS CodeCommit](https://www.aws.training/Details/Video?id=16347)
- [x] [Introduction to AWS CodeBuild](https://www.aws.training/Details/Video?id=16508)
- [x] [Introduction to AWS CodePipeline](https://www.aws.training/Details/Video?id=16441)
- [x] [Introduction to AWS X-Ray](https://www.aws.training/Details/Video?id=16450)

## Exam Readiness

- [ ] [Exam Readiness: AWS Certified Developer – Associate (Digital)](https://www.aws.training/Details/Curriculum?id=19185)
    > Personal key outcomes 
    > 5 domains
      - Deployment (22%)
      - Security (26%)
      - Development with AWS (30%)
      - Refactoring (12%)
      - Monitoring and Troubleshooting (12%)

### Deployment

#### Key knowledges

- AWS Elastic beanstalk
- Serverless
- AWS CloudFormation

#### [Questions samples](./samples/deployment.md)


### Security

#### [Questions samples](./samples/security.md)

### Development with AWS

#### Key knowledges

- DynamoDB
- SNS
- SQS
- AWS Step functions
- API Gateway
- CloudFront
- ElastiCache


#### [Questions samples](./samples/devwithaws.md)

### Refactoring

#### [Questions samples](./samples/refactoring.md)

### Monitoring and Troubleshooting

#### [Questions samples](./samples/monitorandshoot.md)


## Study tips (from Amazon)

### White books

### FAQs

- [SQS](https://aws.amazon.com/fr/sqs/faqs/)

## STOP !

After going through for more than 1 week and reviewing exam samples I consider this certification useless.
You can be a good dev and fail at it, and even worse, you can be absolutly new to dev and pass. Non sense
If you wanna get things done on Amazon, spend time on the particular service you use and get your hands-on it. End of the story
# ECS Service Deployment

This solution will create an ECS cluster and service for a simple application:
* ECS Cluster
* ECS Service
* ECS TaskDefinition
* LaunchConfiguration
* Applicaiton LoadBalancer
* LoadBalancerListener
* TargetGroup
* ListenerRule
* IAM Roles
* IAM InstanceProfile
* SecurityGroup

## Deployment on AWS

This application is deployed using AWS CloudFormation.

#### CloudFormation Parameters: (required)
* InstanceType
* Subnet1
* Subnet2
* VPC

##### Deploy via AWS Console

|Stacks          |Deploy|
|----------------|------|
|ECS Service |<a href="https://console.aws.amazon.com/cloudformation/home#/stacks/new?stackName=ecs-service-cluster&templateURL=https://inf-training-resources.s3.amazonaws.com/ecs-service/ecs-service-cluster.yml" target="_blank">![Launch](./img/launch-stack.png?raw=true "Launch")</a>|
---
#### AWSCLI Deployment scenarios:
* Local bash terminal
* <a href="https://us-west-2.console.aws.amazon.com/cloud9/home?region=us-west-2">Cloud9</a> (Oregon)
* <a href="https://us-west-2.console.aws.amazon.com/cloud9/home?region=us-west-2">Cloud9</a> (Oregon)

#### CloudFormation deployment options:
* Local bash terminal
* <a href="https://us-west-2.console.aws.amazon.com/cloud9/home?region=us-west-2">Cloud9</a> (Oregon)
* <a href="https://us-west-2.console.aws.amazon.com/cloud9/home?region=us-west-2">Cloud9</a> (Oregon)
* <a href="https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1">CloudFormation</a> (N.Virginia)
* <a href="https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1">CloudFormation</a> (N.Virginia)

Create ECR pipeline resources: (add parameters)
```
aws cloudformation deploy --stack-name ecs-service-cluster --template-file cfn/ecs-service-cluster.yml --capabilities CAPABILITY_NAMED_IAM
```

Cleanup:

Delete stack
```
aws cloudformation delete-stack --stack-name ecs-service-cluster
```

## Credits


## License

This library is licensed under the MIT License.

# MATLAB Parallel Server with AWS Batch

# Requirements

Before starting, you must have the following:

* MATLAB Parallel Server license. For more information on how to configure your license for cloud use, see [MATLAB Parallel Server on the Cloud](https://www.mathworks.com/help/licensingoncloud/matlab-parallel-server-on-the-cloud.html).

* MATLAB® and Parallel Computing Toolbox™ on your desktop.

* An AWS account with required permissions. To see what is required, look at the [example policy](matlab-parallel-server-with-aws-batch-admin-IAM-policy.json). For more information about the services used, see [Learn About Cluster Architecture](#learn-about-cluster-architecture).

# Usage Notes
MATLAB Parallel Server with AWS Batch does not support [communicating jobs](https://uk.mathworks.com/help/parallel-computing/introduction.html).

# Costs
You are responsible for the cost of the AWS services used when you create cloud resources using this guide. Resource settings, such as instance type, affect the cost of deployment. For cost estimates, see the pricing pages for each AWS service you are using. Prices are subject to change.

# Introduction
MATLAB® Parallel Server™ with AWS® Batch is a solution for [batch processing MATLAB® jobs](https://www.mathworks.com/help/parallel-computing/batch-processing.html) using Amazon Web Services™ (AWS). The following guide helps you automate the process of launching an AWS Batch cluster in your AWS account. For information about MATLAB Parallel Server, see [Learn About MATLAB Parallel Server](#learn-about-matlab-parallel-server). For information about the architecture of this solution, see [Learn About Cluster Architecture](#learn-about-cluster-architecture).

# Deployment Steps

To view instructions for deploying the MATLAB Parallel Server with AWS Batch reference architecture, select a MATLAB release:

| Release |
| ------- |
| [R2020a](releases/R2020a/README.md) |
| [R2019b](releases/R2019b/README.md) |


# Learn about MATLAB Parallel Server
MATLAB Parallel Server and the Parallel Computing Toolbox lets you solve compute-intensive and data-intensive programs using MATLAB and Simulink on computer clusters, clouds, and grids. Parallel processing constructs such as parallel for-loops and code blocks, special array types, parallel numerical algorithms, and message-passing functions let you implement task-parallel and data-parallel algorithms at a high level in MATLAB. To learn more, see the documentation: [Parallel Computing Toolbox](https://www.mathworks.com/help/parallel-computing) and [MATLAB Parallel Server](https://www.mathworks.com/help/matlab-parallel-server/).

# Learn about cluster architecture
AWS is a set of cloud services which allow you to build, deploy, and manage applications hosted in Amazon’s global network of data centers. Find out more about the range of [cloud-based products offered by AWS](https://aws.amazon.com/products/). You can create, manage, and delete services launched in AWS using the AWS Management Console. For more information about the AWS Management Console, see [AWS Management Console](https://aws.amazon.com/documentation/awsconsolehelpdocs/).

[AWS Batch](https://aws.amazon.com/batch/) is a service for running batch computing jobs on AWS. AWS Batch dynamically provisions, manages, monitors, and terminates [Amazon EC2](https://aws.amazon.com/ec2/) instances based on the volume and resource requirements of the submitted jobs.  Both [On-Demand](https://aws.amazon.com/ec2/pricing/on-demand/) and [Spot](https://aws.amazon.com/ec2/spot/) EC2 instances are supported.  AWS Batch jobs run as containerized applications on [ECS container instances](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/ECS_instances.html).

The cluster architecture and operation of MATLAB Parallel Server with AWS Batch is illustrated in Figure 1.

![Cluster Architecture](img/MATLAB-Parallel-Server-with-AWS-Batch-architecture.png?raw=true)

*Figure 1: Cluster Architecture*

The AWS Batch cluster and the resources required by it are created using [AWS CloudFormation templates](https://aws.amazon.com/cloudformation/).  The resources created by this template are described below. For more information about each resource, see the [AWS CloudFormation template reference.](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-reference.html)

### AWS Batch resources
* Job Definition (AWS::Batch::JobDefinition)  
The job definition specifies how a job is run. It defines the following:
    * The Docker container image to use.
    * The number of virtual CPUS (vCPUS), GPUs, and the amount of memory a job requires.
    * Where to mount the data volume containing the MATLAB installation.
* Compute environment (AWS::Batch::ComputeEnvironment)  
The compute environment used to run jobs. It defines the following:
  * The EC2 pricing model to use (On-Demand or Spot).
  * The launch template to use for EC2 instances.
  * The EC2 instance types to use.
  * The maximum number of vCPUs that can run simultaneously.
  * That the cluster scales down to zero vCPUs when no jobs are in the queue.
* Job Queue (AWS::Batch::JobQueue)  
The job queue to which jobs are submitted. Jobs submitted to the queue run in the defined compute environment.

### S3 bucket
* S3 Bucket for data transfer (AWS::S3::Bucket)  
The S3 bucket used for data transfer between the MATLAB client and the MATLAB workers running in AWS Batch.

### EC2 resources
* Launch template (AWS::EC2::LaunchTemplate)  
The launch template for EC2 instances launched by AWS Batch. Used to mount a MATLAB installation to the EC2 instance.
* Security Group (AWS::EC2::SecurityGroup)  
The security group for EC2 instances launched by AWS Batch.

### Identity and Access Management (IAM) resources
* IAM Role for container instances (AWS::IAM::Role)  
Role that allows containers launched by AWS Batch to access Amazon S3 and Amazon Elastic Container Service.  

* IAM Instance Profile for container instances (AWS::IAM::InstanceProfile)  
Profile that associates containers launched by AWS Batch with the IAM Role for container instances.

* IAM Role for AWS Batch (AWS::IAM::Role)  
Role that provides AWS Batch with the necessary permissions to use other AWS services to run jobs.

* IAM Role for Spot (AWS::IAM::Role)  
Role that provides AWS Batch with the necessary permissions to run jobs using EC2 Spot.

* IAM Role for Lambda function for multiplication (AWS::IAM::Role)  
Role that provides permissions to run the Lambda function for multiplication.

* IAM role for deleting S3 bucket contents (AWS::IAM::Role)  
Role that provides permissions to run the Lambda function to empty S3 bucket.

### Lambda resources
* Lambda function for multiplication (AWS::Lambda::Function)  
Lambda function that multiplies two numbers together. Used to calculate the compute environment's maximum number of vCPUs.

* Custom resource for multiplication (Custom::MultiplyFunction)  
Custom resource that uses the Lambda function for multiplication to calculate the compute environment's maximum number of vCPUs. Multiplies the input parameters "MaxWorkers" and "NumVCPUsPerWorker" together at stack creation.

* Lambda function to empty S3 bucket (AWS::Lambda::Function)  
Lambda function that empties the S3 bucket at stack deletion. When empty, the S3 bucket can be automatically deleted by Cloud Formation.

* Custom resource to empty S3 bucket (Custom::EmptyBuckets)  
Custom resource that uses the Lambda function to empty S3 bucket at stack deletion.

# Technical Support
Email: `cloud-support@mathworks.com`
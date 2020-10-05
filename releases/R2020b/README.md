# MATLAB Parallel Server  with AWS Batch

## Step 1. Launch the Template

Click the **Launch Stack** button for your desired region below to deploy the cloud resources on AWS. This will open the AWS console in your web browser.

| Region | Launch Link |
| --------------- | ----------- |
| **us-east-1** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://us-east-1.console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **us-east-2** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://us-east-2.console.aws.amazon.com/cloudformation/home?region=us-east-2#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **us-west-1** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://us-west-1.console.aws.amazon.com/cloudformation/home?region=us-west-1#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **us-west-2** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://us-west-2.console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **ca-central-1** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://ca-central-1.console.aws.amazon.com/cloudformation/home?region=ca-central-1#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **eu-central-1** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://eu-central-1.console.aws.amazon.com/cloudformation/home?region=eu-central-1#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **eu-west-1** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://eu-west-1.console.aws.amazon.com/cloudformation/home?region=eu-west-1#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **eu-west-2** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://eu-west-2.console.aws.amazon.com/cloudformation/home?region=eu-west-2#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **eu-west-3** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://eu-west-3.console.aws.amazon.com/cloudformation/home?region=eu-west-3#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **eu-north-1** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://eu-north-1.console.aws.amazon.com/cloudformation/home?region=eu-north-1#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **sa-east-1** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://sa-east-1.console.aws.amazon.com/cloudformation/home?region=sa-east-1#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **me-south-1** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://me-south-1.console.aws.amazon.com/cloudformation/home?region=me-south-1#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **ap-east-1** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://ap-east-1.console.aws.amazon.com/cloudformation/home?region=ap-east-1#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **ap-south-1** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://ap-south-1.console.aws.amazon.com/cloudformation/home?region=ap-south-1#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **ap-northeast-1** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://ap-northeast-1.console.aws.amazon.com/cloudformation/home?region=ap-northeast-1#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **ap-northeast-2** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://ap-northeast-2.console.aws.amazon.com/cloudformation/home?region=ap-northeast-2#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **ap-southeast-1** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |
| **ap-southeast-2** | [![alt text](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png "Start an cluster using the template")](https://ap-southeast-2.console.aws.amazon.com/cloudformation/home?region=ap-southeast-2#/stacks/create/review?templateURL=https://matlab-parallel-server-with-aws-batch.s3.amazonaws.com/R2020b/matlab-parallel-server-with-aws-batch.json) |


## Step 2. Configure the Cloud Resources
After you click the Launch Stack button above, the "Quick create stack" page opens in your browser where you can configure the parameters. It is easier to complete the steps if you position these instructions and the AWS CloudFormation console window side by side.

1. Specify a stack name. This will be shown in the AWS CloudFormation console and must be unique within the AWS account.

2. Specify and check the defaults for these resource parameters:

| Parameter label | Description |
| --------------- | ----------- |
| **Container image** | Specify the Docker image to use to execute jobs. This parameter is prepopulated with the default MathWorks Docker image for MATLAB Parallel Server with AWS Batch. Alternatively specify a container repository in the form repository-url/image:tag. |
| **Instance types** | Specify the Amazon EC2 instance types allowed as a comma-delimited list. You can specify instance families (for example, 'c4' or 'p3') or specific sizes within a family (for example, 'c4.8xlarge'). Use 'optimal' to pick instance types on the fly that match the demands of your job queue. For more information on instance types, see https://aws.amazon.com/ec2/instance-types/. |
| **Maximum number of MATLAB workers** | Specify the maximum number of MATLAB workers that the cluster can run concurrently. This number must be less than or equal to the number of workers that your MATLAB Parallel Server license supports. |
| **EC2 pricing model** | Choose either On-Demand or Spot Pricing for the EC2 instances provisioned by AWS Batch. For more information on pricing, see https://aws.amazon.com/ec2/pricing. |
| **Number of GPUs per MATLAB worker** | Specify the number of GPUs for each MATLAB worker to use. If you specify a value greater than 0, you must specify at least one GPU-based instance type supported by AWS Batch in the Instance Types field. For a list of supported GPU-based instance types, see https://docs.aws.amazon.com/batch/latest/userguide/gpu-jobs.html. |
| **Number of vCPUs per MATLAB worker** | Specify the number of vCPUs for each MATLAB worker to use. Two vCPUs per worker is recommended. |
| **Memory per MATLAB worker** | Specify the amount of memory in MiB that each MATLAB worker can use. A minimum of 2000 MiB is required. |
| **Subnets** | Select IDs of existing subnets for the EC2 instances provisioned by AWS Batch. All subnets must exist in the VPC you have selected. It is recommended that you select a subnet for each availability zone in the VPC you have selected. |
| **Spot bid price** | Specify the maximum percentage of On-Demand pricing you want to pay for Spot resources. This parameter is ignored if you select the 'On Demand' EC2 pricing model. |
| **VPC** | Select the ID of an existing VPC in which to deploy this stack. |


*Table 1: Stack input parameters*

3. Tick the box to accept that the template uses IAM roles. These roles provide the following permissions:
 * Allow AWS Batch to make calls to other AWS services in order to run jobs.
 * Allow containers launched by AWS Batch to access Amazon S3 and Amazon Elastic Container Service.
 * Allow a custom lambda function to run that calculates the maximum number of vCPUs for the compute environment.
 * Allow a custom lambda function to run that empties the S3 bucket when the stack is deleted.

4. Click the **Create stack** button.

 When you click Create stack, the cluster is created using AWS CloudFormation templates.  It can take up to five minutes to create the cluster.

5. When the stack status has reached **CREATE_COMPLETE**, select **Outputs**. Figure 1 shows an example of the *Outputs* view.

Identify the values of the outputs with keys 'IndependentJobDefinition', 'JobQueue', 'NumWorkers', and 'S3Bucket' for use in Step 3. If you are an administrator, pass this information to your end users.

    ![Stack outputs on completion](../../img/cloudformation-stack-creation-complete.png)

*Figure 1: Stack outputs on completion*

## Step 3: Connect to the Cluster from MATLAB

If you are an administrator and do not plan to submit jobs to the cluster, you can skip the following steps.
1. Install the [Parallel Computing Toolbox plugin for MATLAB Parallel Server with AWS Batch](https://www.mathworks.com/matlabcentral/fileexchange/72125-parallel-computing-toolbox-plugin-for-matlab-parallel-server-with-aws-batch).  You can also install this plugin via the Add-On Manager in MATLAB.

2. After installation, the Generic Profile Wizard launches in MATLAB.  Use this wizard to configure a cluster profile to connect to the cluster.

    The wizard requires information about the AWS Batch cluster that must be obtained from the values of the stack's outputs. If you are an end user, contact your administrator for this information.  Otherwise, obtain the information from the *Outputs* view of the stack in the CloudFormation console, as described in [Step 2](#step-2-configure-the-cloud-resources).  Table 2 documents the stack output keys that correspond to the wizard field descriptions.

    | **Wizard field description**        | **Stack output key**     |
    | ------------------------------------| -------------------------|
    | Job definition for independent jobs | IndependentJobDefinition |
    | Job queue                           | JobQueue                 |
    | S3 bucket                           | S3Bucket                 |
    | Number of workers                   | NumWorkers               |

    *Table 2: Wizard field descriptions and corresponding stack output keys*

    Complete the wizard to create a cluster profile.

3.  Configure your client machine with your AWS Credentials using the [AWS Command Line Interface tool](https://aws.amazon.com/cli/). Alternatively, you can set up your credentials by setting the environment variables listed in Table 3 on the client machine.  If you do not know your AWS Credentials, contact your administrator.

    | **Environment variable** | **Description** |
    | -------------------------| ----------------|
    | AWS_ACCESS_KEY_ID        | Specifies an AWS access key associated with an IAM user or role.|
    | AWS_SECRET_ACCESS_KEY    | Specifies the secret key associated with the access key. This is essentially the "password" for the access key.|
    | AWS_SESSION_TOKEN        | Specifies the session token value. Required if you are using temporary security credentials.|
    | AWS_DEFAULT_REGION       | Specifies the AWS Region to send the request to.  The value of this environment variable is typically determined automatically but you may wish to set it manually.|

    *Table 3: Environment variables for specifying AWS credentials*

    You can set the environment variables in your current MATLAB session using `setenv` as follows:
    ```matlab
    setenv('AWS_ACCESS_KEY_ID', 'YOUR_AWS_ACCESS_KEY_ID');
    setenv('AWS_SECRET_ACCESS_KEY', 'YOUR_AWS_SECRET_ACCESS_KEY');
    setenv('AWS_SESSION_TOKEN', 'YOUR_AWS_SESSION_TOKEN');
    setenv('AWS_DEFAULT_REGION', 'YOUR_AWS_DEFAULT_REGION');
    ```

4.  (Optional) Open the Cluster Profile Manager. To open the Cluster Profile Manager, on the Home tab, in the Environment section, select *Parallel* > *Create and Manage Clusters...*

    Select the profile created by the wizard.  Validate your cluster by clicking the *Validate* button. The Cluster connection test (parcluster) and Job test (createJob) stages should pass successfully. **The remaining validation stages will not pass as communicating jobs are not supported.**

Your cluster is now set up for [batch processing MATLAB jobs](https://www.mathworks.com/help/parallel-computing/batch-processing.html).  The first time you submit a job to the cluster, MATLAB prompts you to log into your MathWorks account.

### Additional Information

#### Delete Your Cloud Resources

You can remove the CloudFormation stack and all associated resources when you are done with them. Note that there is no undo. After you delete the cloud resources you cannot use the cluster again.

1. Select the stack in the CloudFormation Stacks screen.  Select **Delete**.

2. Confirm the delete when prompted.  It can take a few minutes for CloudFormation to delete your resources.

#### Troubleshooting

If your stack fails to create, check the *Events* section of the CloudFormation console to determine which resources caused the failure and why.
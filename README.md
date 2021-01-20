# AWS Demo

## Step 1: Create an AWS account


Create an AWS account, if you haven't done so already, by going to https://aws.amazon.com/ and choosing Sign Up.


## Step 2: Create or use an IAM user


Create an IAM user or use an existing one in your AWS account. Make sure that you have an AWS access key ID and an AWS secret access key associated with that IAM user. For more information, see [Creating an IAM User in Your AWS Account](https://docs.aws.amazon.com/IAM/latest/UserGuide/Using_SettingUpUser.html).


## Step 3: Use an IAM managed policy to assign CodePipeline permissions to the IAM user


You must give the IAM user permissions to interact with CodePipeline. The quickest way to do this is to apply the AWSCodePipeline_FullAccess managed policy to the IAM user. 


## Step 4: Install the AWS CLI


Install the AWS CLI version 2 on Linux

For the latest version of the AWS CLI, use the following command block:


```bash
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install

```


For a specific version of the AWS CLI, append a hyphen and the version number to the filename. For this example the filename for version 2.0.30 would be awscli-exe-linux-x86_64-2.0.30.zip resulting in the following command:


```bash
curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64-2.0.30.zip" -o "awscliv2.zip"
unzip awscliv2.zip
sudo ./aws/install

```


For a list of versions, see the AWS CLI version 2 changelog
on GitHub. 





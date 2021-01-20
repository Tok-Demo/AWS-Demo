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

aws --version

```


For a list of versions, see the AWS CLI version 2 changelog
on GitHub.


Output:

```bash
aws-cli/2.0.30 Python/3.7.3 Linux/5.4.0-62-generic botocore/2.0.0dev34

```


## Create IAM User



### Create My Policy



### Create My Group

Example:

Group name: ProjectShoppingCart


### Create IAM User


user: iam.{your_mail_name}@gmail.com



#### Setup for HTTPS users using Git credentials



### Create a CodeCommit repository



#### Create New Repository




#### Sign-in credentials


SSH keys for AWS CodeCommit

Use SSH public keys to authenticate access to AWS CodeCommit repositories. [Learn more](http://docs.aws.amazon.com/console/iam/about-ssh-keys) 



#### Connect to the CodeCommit console and clone the repository


On your local machine, use a text editor to create a config file in the ~/.ssh directory, and then add the following lines to the file, where the value for User is the SSH key ID you copied earlier:

[userguide](https://docs.aws.amazon.com/codecommit/latest/userguide/setting-up-ssh-unixes.html)


Update File:

```bash
nano ~/.ssh/config

```


Add SSH config AWS Host


```bash
...
Host ssh://git-codecommit.*.amazonaws.com
  User APKAEIBAERJR2EXAMPLE
  IdentityFile ~/.ssh/id_rsa

# OR

Host git-codecommit.*.amazonaws.com
  User APKAEIBAERJR2EXAMPLE
  IdentityFile ~/.ssh/{codecommit_rsa}


```


#### Add Permissions policies as a IAM User

Add policies

- AWSCodeCommitFullAccess



#### Test SSH Login


```bash
ssh -T  APKAEIBAERJR2EXAMPLE@git-codecommit.ap-southeast-1.amazonaws.com

```

Output:

```bash
You have successfully authenticated over SSH. You can use Git to interact with AWS CodeCommit. Interactive shells are not supported.Connection to git-codecommit.ap-southeast-1.amazonaws.com closed by remote host.

```

#### Add Remote CodeCommit Repo

```bash
ssh-rsa XXXXX
XXXXX== {user}@{client-host}

```


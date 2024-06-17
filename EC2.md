# AWS-Multi-region-Project
Multi-region Web Server Deployment with EBS Volume Management

#### In this project we are going to deploy web server in multi-region and manage the EBS volume.

#### Step 1 :-

Refer the EC2-Configuration file to create EC2 Instance in us-east-1 (North Virginia) region as shown below

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/67570b2d-cbe0-47c1-9168-d16abaf0a7cc)

#### Step 2 :-

Once the instance get launched, connect it and update the instance with the below command

    sudo apt-get update -y

#### Step 3 :-

Now we have to replicate the same instance in the us-west-2 (Oregon) region.

On AWS Console, go to EC2 ==> Instance ==> Select the Instance ==> Action ==> Image and Templates ==> Create Image

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/53547154-c2d1-4d94-aaf3-5808366a9239)

#### Step 4 :-

Go to AMI section. Once Image is "Available" select it and go to Action ==> Copy AMI ==> Select the US West (Oregon) region.

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/4ef15ac9-33c5-4a4d-9cf3-5179b4074506)

Image will get copied in the given region

#### Step 5 :-

Now, Select the Image once it's available and click on Launch instance from AMI

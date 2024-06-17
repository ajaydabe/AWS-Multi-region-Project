### To perform the EBS part of the project follow the below steps

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### Step 1:-

Follow the steps given in EBS-Configuration and create 2 volumes of 10 GiB and 15 GiB

#### Step 2:-

Attach both volumes to the EC2 Instance created in us-east-1 region

#### Step 3:-

Connect to your EC2 Instance

#### Step 4:-

Create File Systems using the below command
      
      sudo mkfs -t xfs /dev/xvdf
      sudo mkfs -t xfs /dev/xvdk

#### Step 5:-


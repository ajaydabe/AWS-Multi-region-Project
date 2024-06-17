### To perform the EBS task of the project, follow the steps given below and mount the volumes

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

#### Step 1:-

Follow the steps given in EBS-Configuration and create 2 volumes of 10 GiB and 15 GiB in us-east-1 region.

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/88dd1841-0d00-4cce-a8b4-0e05d24448e3)

#### Step 2:-

Select Volume ==> Action ==> Attach Volume and select the EC2 Instance created in us-east-1 region.

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/964a5314-66c5-4e4f-bb90-31d290e618c3)

Perform the same step for the another volume and attach it to EC2 Instance.

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/623494f9-9f14-4b24-8ea8-95dc276581ea)

#### Step 3:-

Connect to the EC2 Instance and list the available disk devices to verify the attachment using below command.

      lsblk

#### Step 4:-

Create File Systems using the below command
      
      sudo mkfs -t xfs /dev/xvdf
      sudo mkfs -t xfs /dev/xvdk

#### Step 5:-


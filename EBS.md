### To perform the EBS task of the project, follow the steps given below and mount the volumes

-------------------------------------------------------------------------------------------------------------------------------

#### Step 1 :-

Follow the steps given in EBS-Configuration and create 2 volumes of 10 GiB and 15 GiB in us-east-1 region.

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/cdc3d8d6-a1f3-40ae-a902-cbfd26f35d53)

#### Step 2 :-

Select Volume ==> Action ==> Attach Volume and select the EC2 Instance created in us-east-1 region.

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/dc7cae8d-8747-4245-b34c-1de23db9ce43)

Perform the same step for the another volume and attach it to EC2 Instance.

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/9b0769fd-fca7-43a5-b950-a54dbab89c1c)

#### Step 3 :-

Connect to the EC2 Instance and list the available disk devices to verify the attachment using below command.

      lsblk

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/e245719d-0356-4c34-af13-e5c2882a998c)

#### Step 4 :-

Create File Systems on the volume using the below command
      
      sudo mkfs -t xfs /dev/xvdf
      sudo mkfs -t xfs /dev/xvdk

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/c230eac7-3df9-404c-b1d9-8ef49155e49e)

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/586130b2-a35a-456c-8858-1c15207aea28)

#### Step 5 :-

Create two directories as a mounting points for the volumes using below command

      mkdir VOL-1
      mkdir VOL-2

#### Step 6 :-

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/0dc543d0-fedb-408c-a592-61c18c94c2f7)


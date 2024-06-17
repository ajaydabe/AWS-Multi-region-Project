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

Use below command to mount the volumes on created mounting points

      sudo mount /dev/xvdf VOL-1
      sudo mount /dev/xvdg VOL-2

Verify if the volumes are mounted using the commands:

      lsblk
      df -h

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/0dc543d0-fedb-408c-a592-61c18c94c2f7)

#### Step 7 :- 

So now we need to delete one volume.
The best practice is to 1st unmount the volume, detach it from the EC2 Instance and then delete it.

To unmount the volume use the below command

      sudo umount /dev/xvdf

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/05470856-f3da-4fa4-a2ad-2a47ab7e5293)

Now go to Volume section and detach the same volume from the EC2 Instance and later delete that volume.

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/5b42e2a7-b630-4b05-a6d5-6dd7a81756c0)

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/bd5e180b-c2da-410b-a886-29458578c644)

#### Step 8 :-

Now, extend the size of volume which is still attached to EC2 Instance

![image](https://github.com/ajaydabe/AWS-Multi-region-Project/assets/160045230/5bfb73d2-18fc-46fd-953b-b35b28928533)

#### Step 9 :-


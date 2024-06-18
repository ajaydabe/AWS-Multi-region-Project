## AWS Multi-Region Web Server Deployment with EBS Volume Management

Refer the Task file to understand the project.

Specifications to create EC2 Instance and EBS Volumes are given in EC2-Configurations and EBS-Configurations files.

### Project Flow :-

        Create EC2 Instance in us-east-1 region
                          🡇
          Create Image from the created Instance
                          🡇
          Copy that Image in us-west-2 region
                          🡇
           Launch an Instance from that Image
                          🡇
         Create 2 EBS Volumes in us-east-1 region
                          🡇
          Attach both the EBS Volumes to Instance
               created in us-east-1 region
                          🡇
                   Delete one Volume
                          🡇
           Extend the size of the other Volume
                          🡇
            Take a Snapshot of that Volume

### Conclusion :-

* #### High Availability and Redundancy:

   Multi-region deployment ensures that your web application is resilient to failures in one region.
   By distributing your servers across different geographic locations, you reduce the risk of downtime due to regional outages or disasters.

* #### Latency Optimization:

   Placing servers closer to your users (geographically) can help reduce latency and improve the overall performance of your web application.
   This is particularly important for applications with a global user base.

* #### Data Consistency:

   Managing EBS volumes across multiple regions requires careful consideration of data consistency and synchronization.
   You need strategies such as cross-region replication or distributed databases to ensure that data is up-to-date across all regions.

* #### Disaster Recovery:

   Multi-region deployments are crucial for disaster recovery.
   In case of a catastrophic failure in one region, your application can failover to another region seamlessly if properly configured.

* #### Elastic Block Store (EBS) Management:

   Proper management of EBS volumes involves monitoring performance metrics, optimizing storage configurations (e.g., choosing appropriate volume
   types like General Purpose SSD, Provisioned IOPS SSD, or Magnetic), and implementing backups and snapshots for data protection.

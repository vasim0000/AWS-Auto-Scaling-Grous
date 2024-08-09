# AWS-Auto-Scaling-Grous
As part of my DevOps learning journey, I worked with EFS (Elastic File System) and Auto Scaling Groups, services provided by AWS.

EFS:
It's a fully managed, scalable file storage service that provides shared access to data across multiple Amazon EC2 instances. It automatically scales as you add or remove files.

Auto Scaling:
It monitors the resources by integrating with CloudWatch over the metric, which is used to change the capacity.
1. Adding capacity
2. Removing capacity

=> It uses the EC2 template (AMI) to launch instances when required.
=> It uses the scaling policy to increase or decrease the number of running instances in the group dynamically to meet the changing requirements.

The Auto Scaling contains a few parameters as follows:
1. Minimum size
2. Desired capacity
3. Maximum size

I used the launch template created from an instance to dynamically launch the instances when required. Continuous health checks are performed on these instances; when an instance becomes unhealthy or its load increases with respect to the metric being monitored, the scaling policy of Auto Scaling will terminate the unhealthy instances and create a new healthy instance from the launch template.

Steps to create Auto Scaling groups:

1. Create a launch template.
2. Create a target group for the load balancer.
3. Create the load balancer.
4. Create an auto-scaling group.
5. Select the availability zones and load balancer.
6. Select the parameters (minimum size, desired capacity, maximum size).
   
The scaling policy will dynamically create the desired number of instances, and these get attached to the target group.

![Screenshot (189)](https://github.com/user-attachments/assets/ac727f02-ea8c-48d0-a78e-8b38e34aeead)
![Screenshot (190)](https://github.com/user-attachments/assets/8ab40ba9-1380-4cfa-a81a-78ea203e979e)
![Screenshot (191)](https://github.com/user-attachments/assets/34d6c20e-a968-4cad-8001-99b20055f913)
![Screenshot (192)](https://github.com/user-attachments/assets/d983dad7-1bfe-4eae-a973-0081737c2bd8)





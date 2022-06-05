# CloudDevOps-InfrastructureAsCode-Project - CloudFormation Scripts
Launch Configuration for an application server. I deployed four servers, two located in each of your private subnets. The launch configuration will be used by an auto-scaling group.

In this project, I provisioned the required infrastructure and deployed a dummy application, along with the necessary supporting software.
I have to deploy web servers for a highly available web app using CloudFormation; automating the deployment of the infrastructure and application for an Instagram clone called Udagram.


Script Deployment:

> ./create.sh ProjectUdagram network.yml server-parameters.json

Load Balancer URL:

> http://.us-west-2.elb.amazonaws.com/

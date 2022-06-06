# CloudDevOps-InfrastructureAsCode-Project - CloudFormation Scripts
### Project By Harry Kwabena Ablor
Launch Configuration for an application server. I deployed four servers, two located in each of your private subnets. The launch configuration will be used by an auto-scaling group.

In this project, I provisioned the required infrastructure and deployed a dummy application, along with the necessary supporting software.
I have to deploy web servers for a highly available web app using CloudFormation; automating the deployment of the infrastructure and application for an Instagram clone called Udagram.


Script Deployment:

`./create.sh <stack-name> <template-body>.yml <parameters>.json` 

Example

`./create.sh ProjectUdagram network.yml server-parameters.json` 

Load Balancer URL:

`http://proje-webap-19h03lnccpj0-823753338.us-west-2.elb.amazonaws.com/`

### Changing Instance Size
By default this script will launch your application on t3.small Ubuntu Linux instances with ImageID(AMI ID - ami-0ee8244746ec5d6d4). 
To update this, go to the servers-parameters.json file, change the ParameterValues "InstanceType" to your suitable type.


These files are included in the project:
* /screenshots : Screenshot the result of deploy. 
* create.sh : Create the Cloudformation stack script. 
* update.sh : Update the Cloudformation stack script.
* delete.sh : Delete the Cloudformation stack script.
* network.yml : CloudFormation script template body.
* server-parameters.json : CloudFormation script parameters.



### Dependencies
##### 1. AWS account
You would require to have an AWS account to be able to build cloud infrastructure.

##### 2. VS code editor
An editor would be helpful to visualize the image as well as code. Download the VS Code editor [here](https://code.visualstudio.com/download).

##### 3. An account on www.lucidchart.com
A free user-account on [www.lucidchart.com](www.lucidchart.com) is required to be able to draw the web app architecture diagrams for AWS.


### How to run the supporting material?
You can run the supporting material in two easy steps:
```bash
# Ensure that the AWS CLI is configured before runniing the command below
# Create the network infrastructure
# Check the region in the create.sh file
./create.sh myFirstStack network.yml network-parameters.json
# Create servers
# Change the AMI ID and key-pair name in the servers.yml
# Check the region in the update.sh file
./update.sh mySecStack servers.yml server-parameters.json
```


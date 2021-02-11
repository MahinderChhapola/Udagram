# Udagram
Deploy web servers for a highly available and scalable web app using CloudFormation.

## Architecture Diagram

![Diagram](Project%202.jpeg)

 The network.yml file is used for creating the VPC, Subnets, Internet Gateway etc while passing the network-parameters.json for input parameters. 
 The servers.yml file is used for creating the webservers which include the Load Balancer, AutoScaling Groups, Security Groups, Cloudwatch, IAMRole and server-parameters.json file for parameters. 
 The batch files have been used for creation and updation of the stacks.

## How to run

First create the network by running the create.bat file as below:

```
create Udagram-network network.yml network-parameters.json
```

Then Create the Web server and deploy app by running the create file as shown below.

```
create Udagram-webapp servers.yml server-parameters.json
```

## Webapp Access

Output of the servers.yml will have the LB url.

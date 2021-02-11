# Udagram
Deploy a highly available web application in aws using cloudformation. 

## Architecture Diagram

![Diagram](Project%202.jpeg)

 The **network.yml** file is for creating the network VPC, Subnets, Internet Gateway etc. and **network-parameters.json** for input parameters. 
 The **servers.yml** file is used for creating the webservers which include the Load Balancer, AutoScaling Groups, Security Groups, Cloudwatch, IAMRole and passing the **server-parameters.json** file as the input. 
 There are also a couple of batch files for creation and updation of the stacks. 

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

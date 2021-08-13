## Cloudformation: deploy a HA Web App(IaaC)
The Deploy a high-availability web app using using Cloudformation 


There are included 
Network.yaml,
network-params.json,
ApacheServer.yaml,
ApacheServer-params.json,
VPC diagram.jpeg,
README.md: this file 
create.bat: windows script for cloudformation create stack
update.bat: Windows script for cloudformation update stack


### 1. Network.yaml：

The Network.yaml file is for creating the network VPC, Subnets etc. using the network-params.json as input parameters. 

### 2.ApacheServer.yaml
ApacheServer.yaml using the ApacheServer-params.json file as the input. 
It creates the webservers which include the Load Balancer, 
AutoScaling Groups and Security Groups are created using 

Instructions(Windows 10 )
First create the network by running the create.bat file as below:

create.bat ApacheNetStack Network.yaml network-params.json

Second Create the Web Stack by running the create file as shown below.

create.bat ApacheWebStack ApacheServer.yaml ApacheServer-params.json

### 3. Finally go to "cloudformation"-->"Stacks"--"ApacheWebStack"--"Outputs",
You can get the "LoadBalancerURL",copy the value into your webbrowser.
You will see the website.
URL:
http://apach-WebAp-ARNYONP950OD-1433375166.us-west-2.elb.amazonaws.com






# Project 2 - Deploy a High-Availability Web App using CloudFormation
This directory contains the solution for the project 2 "Deploy a High-Availability Web App using CloudFormation" in the Udacity Nanodegree program "DevOps Engineer". 

## Content
* `Udagram.png` is the infrastructure diagram for the solution.
* In the folder `Screenshots of progress` screenshots for every steps are taken. 
* Screenshot [0 Working Website](https://github.com/damlabeyaz/Udacity_Project2_Deploy-a-High-Availability-Web-App-using-CloudFormation/blob/master/Screenshots%20of%20progress/0%20Working%20Website.png) shows that the web app is working.
* Bash scripts:
	* `create.sh` can be used to create an AWS CloudFormation stack in region `us-east-1`, eg. `sh create.sh servers servers.yml servers-parameters.json`
	* `update.sh` can be used to update an existing AWS Cloudformation stack in region `us-east-1`, e.g `sh update.sh servers servers.yml servers-parameters.json`
	* `delete.sh` can be used to delete an AWS CloudFormation stack, e.g. `sh delete.sh servers`
	* Note: These scripts are specific to a region. You can change them in the script directly or adapt the script to accept a custom region
* CloudFormation scripts:
	* `network.yml` uses `network-parameters.json` to build the whole network under the web app 
	* `servers.yml` uses `servers-parameters.json` to build the web app, load balancer, security groups, IAM configurations and some more stuff (e.g. for Bastion server)
* `udacity.zip` is the content which was uploaded to the AWS S3 bucket

## Application Deployment
To build the whole application stack, run the following commands:

```
% sh create.sh network network.yml network-parameters.json
% sh create.sh servers servers.yml servers-parameters.json
```

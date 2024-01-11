![image](https://github.com/nandineer/AWS_ECR_ECS/assets/22636122/84440e11-56c9-4e8c-8f7d-f1a15109f735)



# Elastic Container Registry


1.	Create Elastic Container registry.
2.	Create a private repository and give a repo name.
3.	Click on the create.
4.	Click on the repo name and push the docker image to the repo.
5.	Use the AWS CLI:

(a)	aws configure

(b)	aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 119357493091.dkr.ecr.us-east-1.amazonaws.com

(c)	docker tag dockerapp:latest 119357493091.dkr.ecr.us-east-1.amazonaws.com/dockerapp:latest

(d)	docker push 119357493091.dkr.ecr.us-east-1.amazonaws.com/dockerapp:latest

6.	Check the image is present in repo.



# Elastic Container Service


7.	Click on create cluster.
8.	Give the cluster name.
9.	For Infrastructure select EC2 or Faragate and click create.
10.	Click on task definition and create new task definition.
11.	Give the task definition name.
12.	For infrastructure select EC2 or Fargate.
13.	For the container 

(a)	Copy the container image from ECR and paste it in image URI
(b)	Give the container name
(c)	Specify the port mapping like 8080, 80.

14.	Click on create.


15.	Click on create service
16.	For compute option click on Launch and verify Infrastructure details
17.	For Deployment configuration select the task name which was created
18.	For Networking select the VPC , subnet and security group.
19.	Ensure the subnet has enable Auto assign IPV4 addresss.
20.	Ensure the security group is allowing all traffic , TCP and HTTP
21.	Click on create.
22.	Navigate to task and click on networking , copy the public ip address and paste on browser.






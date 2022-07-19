### Deploying  Infrastructure as Code (IAC) using AWS Cloud Formation

 ### What is Cloud Formation
  Cloud formation is a service in AWS that one can use to provision infrastructure.It is limited to AWS cloud.
  
  ##### Infrastructure to provision using Cloud Formation
 ![alt text](https://github.com/Ellawangari/DevOps-Diagrams/blob/main/Udacity-ND-DevOps/Udacity-Project2.drawio.png)
  
  #### Prerequisites:
  Have an AWS account.
  Have a user with programmatic access these means has access key and secret key that can be configured using the `aws configure` command.
  Have AWS CLI on VSCode IDE.
  
  
   #### Uses Stacks to provision infrastructure. 
  One can use yaml file to contain the infrastructure to provision code the use a json file to store parameters.
  Before creating a stack it is important to validate your stack.
  ```
  aws cloudformation validate-template --template-body file://network.yaml
  ```
  
  ###### Creating a Stack using the CLI
  
  ```
  aws cloudformation create-stack --stack-name Stack2 --template-body file://webservers.yaml  --parameters file://webservers-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-1
  ```

- So the stack name could be your preferred name.
- Template body file is the path of your yaml file 
- Parameters file is the path of the parameters json file.
- Region could be your AWS account specified region



###### Updating  a Stack using the CLI
```
aws cloudformation update-stack --stack-name Stack2 --template-body file://webservers.yaml  --parameters file://webservers-parameters.json --capabilities "CAPABILITY_IAM" "CAPABILITY_NAMED_IAM" --region=us-east-1
```

###### Deleting  a Stack using the CLI
```
aws cloudformation delete-stack --stack-name $1 
```

#### DNS Output 
 URL `http://stack-webse-1d1zet2pigz77-1454579593.us-east-1.elb.amazonaws.com/`

 Image

 ![alt text](https://github.com/Ellawangari/Udacity-DevopsND/blob/main/imgs/Project2/cloud10.PNG)

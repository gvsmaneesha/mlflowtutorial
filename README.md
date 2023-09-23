# mlflow_tutorial


## For Dagshub:

MLFLOW_TRACKING_URI=https://dagshub.com/gvsmaneesha/mlflowtutorial.mlflow \
MLFLOW_TRACKING_USERNAME=gvsmaneesha \
MLFLOW_TRACKING_PASSWORD=b1c1342e35773597804166f7dd5e80de9bb92f1e \
python script.py


```bash

export MLFLOW_TRACKING_URI=https://dagshub.com/gvsmaneesha/mlflowtutorial.mlflow

export MLFLOW_TRACKING_USERNAME=gvsmaneesha 

export MLFLOW_TRACKING_PASSWORD=b1c1342e35773597804166f7dd5e80de9bb92f1e


```


# MLflow on AWS

## MLflow on AWS Setup:

1. Login to AWS console.
2. Create IAM user with AdministratorAccess
3. Export the credentials in your AWS CLI by running "aws configure"
Also install aws cli in your local machine
4. Create a s3 bucket
5. Create EC2 machine (Ubuntu) & add Security groups 5000 port

Run the following command on EC2 machine
```bash
sudo apt update

sudo apt install python3-pip

sudo pip3 install pipenv


sudo pip3 install virtualenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell


## Then set aws credentials
aws configure


#Finally 
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-23

#open Public IPv4 DNS to the port 5000


#set uri in your local terminal and in your code 
export MLFLOW_TRACKING_URI=ec2-54-254-222-233.ap-southeast-1.compute.amazonaws.com:5000/
```


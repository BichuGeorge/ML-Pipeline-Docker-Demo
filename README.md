# End-to-End-Machine-Learning-Pipeline


## Workflows

1. Update config.yaml
2. Update schema.yaml
3. Update params.yaml
4. Update the entity
5. Update the configuration manager in src config
6. Update the components
7. Update the pipeline 
8. Update the main.py
9. Update the app.py



# How to run?
### STEPS:

Clone the repository

```bash
https://github.com/BichuGeorge/ML-Pipeline-Docker-Demo
```
### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n mlproj python=3.8 -y
```

```bash
conda activate mlproj
```


### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


```bash
python app.py
```



# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. Azure VM access : It is virtual machine

	2. ACR: Azure Container registry to save your docker image in azure


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ACR

	3. Launch Your Azure VM 

	4. Pull Your image from ACR in Azure VM

	5. Lauch your docker image in Azure VM


	
## 3. Create ACR login user:
    - Save the URI: winerepo.azurecr.io

	
## 4. Create Azure VM machine (Ubuntu) 

## 5. Open Azure VM and Install docker in azure VM Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure VM as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

    AZURE_CLIENT_ID

	AZURE_CLIENT_SECRET

	AZURE_TENANT_ID

	The above 3 can be fetched using command: 
	az ad sp create-for-rbac --name "gh-actions-sp" --role contributor --scopes /subscriptions/<SUBSCRIPTION_ID> --sdk-auth

    ACR_NAME — name of your Azure Container Registry (e.g. myregistry)
	ACR_LOGIN_SERVER — full login server (e.g. myregistry.azurecr.io)
	ACR_REPOSITORY_NAME — repository/image name (e.g. cnncls)

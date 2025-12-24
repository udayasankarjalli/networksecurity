### Network Security Projects For Phising Data
project structure:
constant/training-pipeline:where we can define all stages constant values.
entity/artifactentity:those constant entities define by using dataclass.
entity/configentity:do configuration/intialise required constant values by calling constant/training-pipeline
components: write each stage required classes with defined functions to achieve that stage functionalities.
utils:where we can define all our common functionalities which we can use anywhere.
Main.py : From here we can call required classes/modules to execute each stage functionality.
Artifacts:where we can create each stage artifacts folder with name and store artifacts.
data_schema :where we can mention data file shema,by using this we can validate data and check drift
exceptions&logging: we mention our customized logging info in logging& define customized exceptions in exception folder/file.

Setup github secrets:
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = us-east-1

AWS_ECR_LOGIN_URI = 788614365622.dkr.ecr.us-east-1.amazonaws.com/networkssecurity
ECR_REPOSITORY_NAME = networkssecurity


Docker Setup In EC2 commands to be Executed
#optinal

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker
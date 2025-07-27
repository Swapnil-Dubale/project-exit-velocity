
ssh -i "exit-velocity-key.pem" ubuntu@ec2-13-62-76-140.eu-north-1.compute.amazonaws.com

AKIAQMEY5XJVHCVSISFI

created an ec2 instance (ubuntu)  exit_velocity
launched it and ssh into it using "exit-velocity-key.pem" key created at the time of instance creation
created S3 bucket exit-velocity-s3-bucket
uploaded a text file using UI from web
To interact with s3 from aws cli I had to install - sudo snap install aws-cli --classic
then I created a IAM user swapy with AdministratorAccess permission policy

then ran aws configure command to setup the configuration to interact with s3
after giving access key, secret key of IAM user and region of EC2 I was able to executes3 commands

 sudo snap install aws-cli --classic
   15  aws s3 ls
   16  aws configure
   17  aws s3 ls
   18  aws configure
   19  aws s3 ls
   20  aws configure
   21  aws s3 ls
   22  ls -lrt
   23  aws s3 cp hello.sh s3://exit-velocity-s3-bucket/
   24  aws s3 ls s3://exit-velocity-s3-bucket/
   25  mkdir DownloadFromS3
   26  ls
   27  as s3 cp s3://exit-velocity-s3-bucket/hello.txt.txt ./DownloadFromS3/
   28  aws s3 cp s3://exit-velocity-s3-bucket/hello.txt.txt ./DownloadFromS3/
   29  ls
   30  cd DownloadFromS3/
   31  ls
   32  exit

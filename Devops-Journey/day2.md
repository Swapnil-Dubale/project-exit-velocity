Created an IAM role and created a IAM policy that give read only access to EC2 and 
S3 -> generated Access key and secret and used it to configure 'aws configure'
locally with this IAM user

created IAM Role for EC2 instance and created new policy that has full access to 
s3 and attached that policy to this role by adding permissions ans selecting hte created 
policy

 533766c625eb4adf9d478d3f22bd416d
--------------------------
installed java jdk and jenkins on ec2 , had to open 8080 port from security group allowing traffic from anywhere 
IPv4

 which java
   64  cd
   65  cd /usr/lib/jvm
   66  ls
   67  cd java-11-openjdk-amd64
   68  pwd
   69  cd ../openjdk-11
   70  ls
   71  cd ..
   72  ls
   73  cd java-1.11.0-openjdk-amd64
   74  ls
   75  pwd
   76  export JAVA_HOME=/usr/lib/jvm/java-1.11.0-openjdk-amd64
   77  echo $JAVA_HOME


aws s3 ls
aws ec2 describe-instance
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee   /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]   https://pkg.jenkins.io/debian-stable binary/ | sudo tee   /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt install openjdk-17-jdk -y
sudo systemctl status jenkins
sudo journalctl -xeu jenkins.service -> to check jenkins logs
ubuntu@ip-172-31-36-172:~$ sudo lsof -i :8080  -> check if anything running on port 8080
ubuntu@ip-172-31-36-172:~$ sudo systemctl restart jenkins
ubuntu@ip-172-31-36-172:~$ sudo systemctl status jenkins

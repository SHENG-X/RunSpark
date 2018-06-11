
# Run a Spark cluster on AWS EC2

## Installing java

Check Java Version: &nbsp;&nbsp;&nbsp;`java -version`

Updata Packages: &nbsp;&nbsp;&nbsp;`sudo apt-get update` 

Install JDK: &nbsp;&nbsp;&nbsp;`sudo apt-get install default-jdk`
 

## Install Scala

`sudo apt-get install scala`

## Install Spark

  

Download From: [https://spark.apache.org/downloads.html](https://spark.apache.org/downloads.html)

  

![Screenshot]('/ss1.png'  "Download Spark")

  

Command For Download Spark: `wget https://archive.apache.org/dist/spark/spark-1.6.0/spark-1.6.0-bin-hadoop2.6.tgz`

  

Unzip Spark: `tar xvf spark-1.6.0-bin-hadoop2.6.tgz`

  

## Setup Spark Environment

+ Find `spark-ec2` file in `ec2 folder`

+ Modify `python -Wdefault "${SPARK_EC2_DIR}/spark_ec2.py" "$@"`__to__  `python3 -Wdefault "${SPARK_EC2_DIR}/spark_ec2.py" "$@"`
+ Move .pem file from local machine to ec2 folder on server
+ Export AWS_ACCESS_KEY_ID AND AWS_SECRECT_ACCESS_KEY:
	+ `export AWS_ACCESS_KEY_ID=DJAKFNANFKLWCPGNHA`
	+ `export AWS_SECRECT_ACCESS_KEY=bN120Nnna12190jfqfioPEFZL9`
+ Change .pem file permission `chmod 400 "aws4980.pem"`
+ Launch Clusters:  `./spark-ec2 --key-pair=aws4980 --identity-file=aws4980.pem --region=us-west-2 --zone=us-west-2a -s 8 --instance-type=t2.micro launch sheng4980`

# Working Screenshoots
![Screenshot]('/ss2.png'  "Spark Running")

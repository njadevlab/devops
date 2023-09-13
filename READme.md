
Apache Maven Installation And Setup In AWS EC2 Redhat Instance.
1. Install JAVA
		sudo hostnamectl set-hostname maven
		sudo su - demo  
		cd /opt
		sudo apt install wget nano tree unzip git-all -y
		sudo apt install default-jre  && default-jdk -y
		java -version
		git --version

2. Downloand and Install Maven
		sudo wget https://dlcdn.apache.org/maven/maven-3/3.9.4/binaries/apache-maven-3.9.4-bin.zip
		sudo unzip apache-maven-3.9.4-bin.zip
		sudo rm -rf apache-maven-3.9.4-bin.zip
		## Rename the extracted folder for a good naming convention
		sudo mv apache-maven-3.9.4/ maven

3. Set Environmental Variable
		## Edit the bash_profile. Add the following
		ls -a /home/demo/
		vi ~/.bash_profile 
		export M2_HOME=/opt/maven
		export PATH=$PATH:$M2_HOME/bin

4. Refresh the profile and verify Maven is running
		source ~/.bash_profile
		mvn -version

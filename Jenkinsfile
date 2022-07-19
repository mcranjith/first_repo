pipeline {
    agent {label 'tomcat-slave'}

    stages {
        stage('Git checkout') {
		steps {
				git 'https://github.com/kishancs2020/webAppExample.git'
				}
		}
		stage('Build stage') {
		steps {
		sh 'mvn clean install' }
		}
		stage('push to artifactory') {
		steps {
		sleep 10 }
		}
		stage('Deploy') {
		steps 
			{sh 'sudo cp /home/ec2-user/Jenkins-slave/workspace/first-pipeline/target/*.war /opt/apache-tomcat-9.0.64/webapps/'
			}
		
		}
		}
		
		}

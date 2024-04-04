pipeline {
    agent any
    
    stages {
        stage('checkout code') {
            steps {
                git branch: 'main', url: 'https://github.com/technicalsoumya/java-web-app.git'
            }
        }
        stage('build code') {
            steps {
                sh '/opt/maven/bin/mvn clean package'
            }
        }
        stage('Deployment'){
			steps{
				deploy adapters: [ tomcat9(url: 'https://54.196.210.94:8080/', credentialsId: 'my-cred')], war:'**/*.war'
			}
		}
    }
}

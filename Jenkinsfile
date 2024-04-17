pipeline {
    agent {
        node{
          label 'jenkins-slave-node-1'
        }
    }
        stages {
            stage ('checkout code') {
                steps {
                    git branch: 'main' , url: 'https://github.com/technicalsoumya/java-web-app.git'
                }
            }
            stage ('Build code') {
                steps {
                    sh '/opt/maven/bin/mvn clean package'
                }
            }
            stage ('deploy to tomcat') {
                steps {
                    deploy adapters: [tomcat9(url: 'http://54.89.204.236:8080/', credentialsId: 'jenkins-cred')], war: '**/*.war'
                }
            }
        }
    
}
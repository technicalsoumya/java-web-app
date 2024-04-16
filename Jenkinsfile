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
        }
    
}
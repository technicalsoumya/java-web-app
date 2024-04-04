pipeline{
    agent {
        node {
            label 'slave-node'
        }
    }
    stages {
        stage ('checkout code'){
            steps {
                git branch: 'main', url: 'https://github.com/technicalsoumya/java-web-app.git'
            }
        }
        stage ('build code'){
            steps{
                sh '/opt/maven/bin/mvn clean package'
            }
        }

    
    }
}
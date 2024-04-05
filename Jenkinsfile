node{
    stage ('checkout code') {
        git branch:'main', url:'https://github.com/technicalsoumya/java-web-app.git'
    }
    stage ('build Code') {
        sh '/opt/maven/bin/mvn clean package'
    }
    stage ('deploy to tomcat') {
        deploy adapters:[tomcat9(url:'', credentialsId:'tomcat-cred')], war:'**/*.war'

    }
}
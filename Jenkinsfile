node{
    stage ('checkout code') {
        git branch:'main', url:'https://github.com/technicalsoumya/java-web-app.git'
    }
    stage ('build Code') {
        sh '/opt/maven/bin/mvn clean package'
    }
    stage ('deploy to tomcat') {
        deploy adapters:[tomcat9(url:'http://54.198.233.109:8080', credentialsId:'tomcat-cred')], war:'**/*.war'

    }
}
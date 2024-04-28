pipeline {
    agent {
        node {
            label 'jenkins-slave-node'
        }
    }
    environment {
        PATH = "/opt/maven/bin:$PATH"
    }
    stages {
        stage("checkout code"){
            steps {
                echo "----------- checkout started ----------"
                git branch: "main" , url: "https://github.com/technicalsoumya/java-web-app.git"
                echo "----------- checkout completed ----------"
            }
        }
   }
   stages {
       stage( "build code"){
           steps {
               echo " ---------build started--------"
               sh "mvn clean package -Dmaven.test.skip= true"
               echo " ---------build completed-------" 
        }
      }
   }

}

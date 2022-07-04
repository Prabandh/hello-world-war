pipeline {
    agent any
    stages { 
        stage('Clone') {
            steps {
                sh 'rm -rf hello-world-war'
             sh 'git clone https://github.com/Prabandh/hello-world-war.git'
            }
        }
            stage('building') {
            steps {
             sh 'mvn package'
            }
         }
     stage('deploying') {
            steps {
              sh 'sudo cp /home/jenkins-slave1/workspace/target/hello-world-war-1.0.0.war /opt/apache-tomcat-9.0.64/webapps/'
            }
        }
    }
}

pipeline {
    agent any
    parameters {
        choice(name: 'choices', choices: ['one', 'two'])
    }
    stages { 
        stage('Clone') {
            steps {
                sh 'rm -rf hello-world-war'
             sh 'git clone https://github.com/Prabandh/hello-world-war.git'
            }
        }
            stage('mouse') {
            steps {
             sh 'mvn package'
            }
         }
     stage('deploying') {
            steps {
              sh 'sudo cp /var/lib/jenkins/workspace/pipe_ex/target/hello-world-war-1.0.0.war /opt/apache-tomcat-9.0.64/webapps/'
            }
        }
    }
}

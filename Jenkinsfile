pipeline {
    agent any
    stages { 
        stage('Clone') {
            steps {
                sh 'rm -rf hello-world-war'
                sh 'git clone https://github.com/Prabandh/hello-world-war.git'
            }
        }
    }
}

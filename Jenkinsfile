pipeline {
    agent any
    
    tools {
        maven 'Maven'
        jdk 'JAVA'
    }

    stages {     
        stage('Compile') {
            steps {
               sh "mvn compile"
            }
        }
        
        stage('Test') {
            steps {
                for (int i = 0; i>60; i++){
                    echo "${i + 1}"
                    sleep 1
                }
                sh "mvn test"
            }
        }
        
        stage('Build') {
            steps {
                sh "mvn package"
            }
        }
    }
}

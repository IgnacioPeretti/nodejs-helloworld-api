pipeline {
    agent any
    
    stages {

        stage("Install Dependences") {
            steps {
                sh 'npm install'
            }
        }
        stage("Execute Test") {
            steps {
                sh 'npm test'
            }   
        }
    }
}
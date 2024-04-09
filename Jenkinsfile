pipeline {
    agent any
    
    stages {
        stage("Clonammos el repositorio") {
            steps {
                git 'https://github.com/edgaregonzalez/nodejs-helloworld-api.git'
            }
        }
        stage("Instalar Dependencias") {
            steps {
                sh 'npm install'
            }
        }
        stage("Ejecutar Pruebas") {
            steps {
                sh 'npm test'
            }   
        }
    }
}
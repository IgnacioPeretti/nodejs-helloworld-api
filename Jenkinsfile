pipeline {
    agent any
    
    stages {
        stage("Clonamos el repositorio") {
            steps {
                git clone 'https://github.com/edgaregonzalez/nodejs-helloworld-api.git'
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
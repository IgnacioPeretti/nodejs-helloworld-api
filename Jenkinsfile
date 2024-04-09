pipeline {
    agent any

    stages {
        stage("Clonamos el repositorio") {
            steps {
                sh git clone 'https://github.com/edgaregonzalez/nodejs-helloworld-api.git'
            }
        }
        stage("Instalar Dependencias") {
            steps {
                sh 'npm install'
            }
        }
        stage("Ejecutar Test") {
            steps {
                sh 'npm test'
            }   
        }
    }
}
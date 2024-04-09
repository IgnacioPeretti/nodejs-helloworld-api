pipeline {
    agent any
    
    stages {

        stage("Instalar Dependencias") {
            steps {
                sh 'npm install'
            }
        }
        stage("Ejecutando Pruebas") {
            steps {
                sh 'npm test'
            }   
        }
    }
}
pipeline {
    agent any
    
    stages {

        stage("Instalando Dependencias") {
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
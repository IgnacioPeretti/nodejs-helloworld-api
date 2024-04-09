pipeline {
    agent any
    
    stages {
        
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
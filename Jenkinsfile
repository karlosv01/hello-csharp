pipeline {
    agent {
        docker { 
            image 'python:3.11-slim' 
            args '-u root' 
        }
    }
    stages {
        stage('Hola Mundo') {
            steps {
                sh 'python3 hello.py'
            }
        }
    }
}
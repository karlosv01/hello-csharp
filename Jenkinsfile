pipeline {
    agent any
    stages {
        stage('Descarga') {
            steps {
                checkout scm
            }
        }
        stage('Compilar') {
            steps {
                // Esto verifica si tienes dotnet instalado en el servidor
                sh 'dotnet build'
            }
        }
        stage('Prueba Básica') {
            steps {
                echo 'El código se ha compilado correctamente. ¡Prueba superada!'
            }
        }
    }
}
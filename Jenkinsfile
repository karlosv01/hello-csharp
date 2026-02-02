pipeline {
    agent any
    stages {
        stage('Limpieza') {
            steps {
                echo 'Limpiando el espacio de trabajo...'
                deleteDir()
            }
        }
        stage('Descarga de Código') {
            steps {
                checkout scm
            }
        }
        stage('Ejecutar Python') {
            steps {
                // En Linux, Python 3 se suele llamar con 'python3'
                sh 'python3 hello.py'
            }
        }
        stage('Prueba de Versión') {
            steps {
                sh 'python3 --version'
                echo '¡Pipeline de Python completado con éxito!'
            }
        }
    }
}
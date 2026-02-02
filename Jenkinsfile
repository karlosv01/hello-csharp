pipeline {
    agent {
        docker { 
            // Usamos el SDK de .NET 8 (o la versión que prefieras)
            image 'mcr.microsoft.com/dotnet/sdk:8.0' 
            args '-u root' 
        }
    }
    stages {
        stage('Restaurar y Compilar') {
            steps {
                // Descarga las librerías necesarias y compila el ejecutable
                sh 'dotnet restore'
                sh 'dotnet build'
            }
        }
        stage('Ejecutar C#') {
            steps {
                // Ejecuta tu programa
                sh 'dotnet run'
            }
        }
    }
}
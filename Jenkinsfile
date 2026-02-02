pipeline {
    agent {
        docker { 
            image 'mcr.microsoft.com/dotnet/sdk:8.0' 
            args '-u root' 
        }
    }
    stages {
        stage('Compilar') {
            steps {
                // Compilamos en modo Release (optimizado)
                sh 'dotnet publish -c Release -o ./publish'
            }
        }
    }
    post {
        success {
            // Esto guarda todo lo que haya en la carpeta publish
            archiveArtifacts artifacts: 'publish/**', fingerprint: true
            echo '¡Artefacto guardado correctamente!'
        }
    }
}
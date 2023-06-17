pipeline {
    agent {
        docker {
            image 'node:16-buster-slim' 
            args '-p 8000:8000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
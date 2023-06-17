node {
    agent {
        docker {
            image 'node:16-buster-slim'
            args '-p 8000:8000'
        }
    }
    stage('Build') { 
        sh 'npm install' 
    }
}
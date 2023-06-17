node {
    docker.image('node:16-buster-slim').inside(' -p 8000:8000') {
        stage('Build') { 
            sh 'npm install' 
        }
        stage('Test') { 
            sh 'npm run test' 
        }
    }
}
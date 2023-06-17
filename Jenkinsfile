docker.image('node:16-buster-slim').withRun(' -p 8000:8000') {
    node {
        stage('Build') { 
            sh 'npm install' 
        }
    }
}
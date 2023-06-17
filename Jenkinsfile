node {
    docker.image('node:16-buster-slim').inside(' -p 7000:7000') {
        stage('Build') { 
            sh 'npm install' 
        }
        stage('Test') { 
            sh 'npm run test' 
        }
    }
}
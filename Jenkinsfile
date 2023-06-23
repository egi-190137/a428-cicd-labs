node {
    docker.image('node:lts-buster-slim').inside(' -p 3000:3000') {
        stage('Build') { 
            sh 'npm install' 
        }
        stage('Test') { 
            sh 'npm run test' 
        }
        stage('Manual Approval') {
            input message: 'Lanjutkan ke tahap Deploy?”'
        }
        stage('Deploy') {
            sh './jenkins/scripts/deliver.sh'
            sh 'sleep 1m'
            sh './jenkins/scripts/kill.sh'
        }
    }
}
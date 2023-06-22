node {
    docker.image('node:18-buster-slim').inside(' -p 3000:3000') {
        stage('Build') { 
            sh 'npm install' 
        }
        stage('Test') { 
            sh 'npm run test' 
        }
        stage('Deploy') {
            sh './jenkins/scripts/deliver.sh'
            input message: 'Sudah selesai menggunakan React App? (Klik "proceed" untuk mengkahiri)'
            sh './jenkins/scripts/kill.sh'
        }
    }
}
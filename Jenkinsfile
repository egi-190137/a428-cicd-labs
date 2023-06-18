node {
    docker.image('node:16-buster-slim').inside(' -p 7000:7000') {
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
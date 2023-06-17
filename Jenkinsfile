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
29bde3b5d1d7ecca38ff9d8005f53ff53a75ea3f 
fb619b2f073de29ba5c87c70615660e0e2bdc015
pipeline {
    agent {
        docker { image 'node:10-alpine' }
    }
    stages {
        stage('Npm install') {
            steps {
                sh 'npm install'
            }
        }           
    }
}
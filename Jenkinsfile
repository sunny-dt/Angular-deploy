pipeline {
    agent {
        docker { image 'node:10-alpine' }
    }
    stages {
        stage('SCM Checkout'){
            git 'https://github.com/sunny-dt/Angular-deploy.git'
        }
        stage('Restore') {
            steps {
                sh 'npm install'
            }
        }           
    }
}
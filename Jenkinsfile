pipeline {
    agent {
        docker {
            image 'node:6-alpine'
            args '-p 4000:3000'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
        post {
            always {
                junit '**/target/*.xml'
            }
            failure {
                mail to: sunny@digitaltaas.com, subject: 'The Pipeline failed :('
            }
        }
    }
}
pipeline {
    agent {
    docker {
            image 'node:6-alpine' 
        }}
    }
    stages {
        stage('Dependencies') {
            steps {
                sh 'npm i'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Unit Tests') {
            steps {
                sh 'npm run test'
            }
        }
        stage('e2e Tests') {
            steps {
                sh 'npm run cypress:ci'
            }
        }
        stage('Deploy') {
            steps {
               checkout scm
                docker.withRegistry('http://localhost:50000/') {
                // def customImage = docker.build("my-image:${env.BUILD_ID}")
                def customImage = docker.build("beam-angular-app-image")
                /* Push the container to the custom Registry */
                customImage.push()
                }
            }
        }
    }

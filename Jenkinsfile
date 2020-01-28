pipeline {
    agent {
        dockerfile true
    }
    stages {
        stage ('one'){
            steps {
                sh 'node --version'
                sh 'svn --version'  
            }
        }
    }

}
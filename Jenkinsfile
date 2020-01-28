pipeline {
    agent {
        dockerfile true
    }
    stages {
        stage ('one'){
            steps {
                echo 'Testing jenkinsfile'
            }
        }
        stage ('two'){
            steps{
                input(' Do you want to proceed')
            }
        }
    }

}
pipeline {
    agent any
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
        stage('three'){
            when {
                not {
                    branch 'master'
                }
            }
            steps{
                echo 'Hello from branch'
            }
        }
    }

}
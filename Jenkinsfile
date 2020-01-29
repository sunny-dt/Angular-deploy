pipeline{
    agent { label 'nodejs8' }
    stages{
        stage('SCM Checkout'){
        git 'https://github.com/sunny-dt/Angular-deploy.git'
    }
    stage ('install modules'){
      steps{
        sh '''
          npm install --verbose -d 
          npm install --save classlist.js
        '''
      }
    }
    }
}
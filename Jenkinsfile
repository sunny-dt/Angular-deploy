node {
    stage('SCM Checkout'){
        git 'https://github.com/sunny-dt/Angular-deploy.git'
    }
    stage('Node package install'){
        sh label: 'dependecies', script: 'npm i'
    }
    stage('Build docker image'){
        sh 'docker build -t localhost:50000/angular-ci-image .'
    }
}
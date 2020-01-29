node {
    stage('SCM Checkout'){
        git 'https://github.com/sunny-dt/Angular-deploy.git'
    }
    stage('Node package install'){
        sh label: 'dependecies', script: 'npm i'
    }
}
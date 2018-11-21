pipeline {
    agent { docker { image 'nodesource/trusty:5.1' } }
    environment {
        HOME = "."
    }
    stages {
        stage('pre-build'){
            steps {
              sh 'npm cache clean --force'
            }
        }
        stage('build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
    }
}
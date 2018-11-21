pipeline {
    agent { docker { image 'node:6-alpine' } }
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
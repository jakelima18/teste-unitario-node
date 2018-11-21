pipeline {
    agent { docker { image 'node:6-alpine' } }
    environment {
        HOME = "."
    }
    stages {
        stage('pre-build'){
            steps {
              sh 'npm cache clean'
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
pipeline {
    agent { docker { image 'node:6-alpine' } }
    environment {
        HOME = "."
    }
    stages {
        stage('pre-build'){
            steps {
              sh 'npm cache clear'
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
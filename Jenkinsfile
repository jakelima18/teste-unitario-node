pipeline {
    agent { docker { image 'nodesource/trusty:5.1' } }
    environment {
        HOME = "."
    }
    stages {
        stage('build') {
            steps {
                sh 'npm install'
            }
        }
    }
}
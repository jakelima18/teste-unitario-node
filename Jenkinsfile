pipeline {
    agent {
        docker {
            image 'node'
            args '-p 3000:3000'
        }
    }
    environment {
        HOME = '.' 
    }
    stages {
        stage('Build') {
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
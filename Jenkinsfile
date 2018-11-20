pipeline {
    agent {
        docker {
            image 'docker pull woorank/docker-node-babel'
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
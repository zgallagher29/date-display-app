pipeline {
    agent {
        docker { image 'node:carbon-jessie' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    }
}
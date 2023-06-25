pipeline {
    agent {
        docker { image 'node:18.16.0-alpine' }
        reuseNode true
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    }
}

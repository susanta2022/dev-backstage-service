pipeline {
    agent {
        docker {
            image 'python:3.9' // Specify the Python version you need
        }
    }
    
    stages {
        // ...
        
        stage('Deploy') {
            steps {
                sh 'python test.py' // Build a Docker image for your application
                
                
            }
        }
    }
}

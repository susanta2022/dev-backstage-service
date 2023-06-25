pipeline {
    agent none 
    
    stages {
        // ...
        
        stage('Deploy') {
            agent {
                    docker {
                    image 'python:3.9' // Specify the Python version you need
                    } 
            }
            
            steps {
                sh 'python tset.py' // Build a Docker image for your application             
                
            }
        }
    }
}

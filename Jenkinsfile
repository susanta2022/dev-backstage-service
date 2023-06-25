pipeline {
    agent any
    
    stages {
        // ...
        
        stage('Deploy') {
            steps {
                sh 'docker build -t myapp .' // Build a Docker image for your application
                
                sh 'docker run --name myapp-container myapp python test.py' // Run the Python file in a Docker container
            }
        }
    }
}

pipeline {
    agent any
    
    stages {
        // ...
        
        stage('Deploy') {
            steps {            
                
                sh 'docker run --rm -v $PWD:/app -w /app python:3.9 python test.py' // Run the Python file in a Docker container
            }
        }
    }
}

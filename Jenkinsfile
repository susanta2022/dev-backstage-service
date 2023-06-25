pipeline {
    agent any 
    
    stages {
        stage('Checkout') {
      steps {
        script {
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], userRemoteConfigs: [[url: 'https://github.com/susanta2022/dev-backstage-service.git']]])
        }
      }
    }        
      stage('Deploy') {
            agent {
                    docker {
                    image 'python:3.9' // Specify the Python version you need
                    } 
            }
            
            steps {
                sh 'python main.py' // Build a Docker image for your application             
                
            }
        }

      stage('Test') {
            agent {
                    docker {
                    image 'python:3.9' // Specify the Python version you need
                    } 
            }
            
            steps {
                sh 'python main-test.py' // Build a Docker image for your application             
                
            }
        }
        
    }
}

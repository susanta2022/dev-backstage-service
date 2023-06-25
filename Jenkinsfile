pipeline {
    agent any 
    
    stages {
        stage('Checkout') {
      steps {
        script {
            checkout([$class: 'GitSCM', branches: [[name: '*/mast']], userRemoteConfigs: [[url: 'https://github.com/susanta2022/dev-backstage-service.git']]])
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
                sh 'python tset.py' // Build a Docker image for your application             
                
            }
        }
    }
}

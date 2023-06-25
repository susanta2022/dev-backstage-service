pipeline {
  agent { docker { image 'python:3.9' } }
  stages {
    stage('build') {
       environment
      {
        HOME="//$PWD"
      }
      steps {
        sh 'pip install boto3'
      }
    }
    stage('test') {
      environment
      {
        HOME="//$PWD"
      }
      steps {
        sh 'python test.py'
      }   
    }
  }
}

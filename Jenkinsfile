pipeline {
  agent { docker { image 'python:3.9' } }
  stages {
    stage('build') {
       environment
      {
        HOME="."
      }
      steps {
        sh 'pip install boto3'
      }
    }
    stage('test') {
      environment
      {
        HOME="."
      }
      steps {
        sh 'python test.py'
      }   
    }
  }
}

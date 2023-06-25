pipeline {
  agent { docker { image 'python:3.9' } }
  stages {
    stage('build') {
      steps {
        sh 'pip install boto3'
      }
    }
    stage('test') {
      steps {
        sh 'python test.py'
      }   
    }
  }
}

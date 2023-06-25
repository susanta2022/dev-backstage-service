pipeline {
  agent none
  stages {
    stage('Docker Test') {
      agent {
        dockerfile {
          filename 'Dockerfile'
          label 'windocker'
        }
      }
      steps {
        println 'Hello, World!'
      }
    }
  }
}

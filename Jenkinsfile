stage('build') {
  node('docker&&windows'){
    bat 'echo NodeName = %COMPUTERNAME%'
    docker.image('microsoft/windowsservercore:10.0.14393.206').inside {
      bat 'echo %COMPUTERNAME% > container_computername.txt'
    }
  }
}

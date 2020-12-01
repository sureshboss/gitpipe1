pipeline {
  agent any
  stages {
    stage('Begin') {
      steps {
        powershell 'echo "hi env:name how are you?"'
      }
    }

  }
  environment {
    name = 'suresh'
    team = 'raiseit2.0'
    dept = 'imsauto'
  }
}
pipeline {
  agent any
  stages {
    stage('Begin') {
      steps {
        powershell(script: '$name=$env:name;echo "hi $name how are you?"', label: 'msg')
      }
    }

    stage('print') {
      steps {
        echo '${msg}'
      }
    }

  }
  environment {
    name = 'suresh'
    team = 'raiseit2.0'
    dept = 'imsauto'
  }
}
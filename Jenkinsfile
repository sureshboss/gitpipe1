pipeline {
  agent any
  stages {
    stage('Hostname') {
      steps {
        powershell(script: 'hostname', returnStatus: true, returnStdout: true, label: 'labelname')
      }
    }

    stage('Sleep') {
      steps {
        sleep 160
        echo 'WakedUp'
      }
    }

  }
}
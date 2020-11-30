pipeline {
  agent any
  stages {
    stage('Hostname') {
      parallel {
        stage('Hostname') {
          steps {
            powershell(script: 'hostname', returnStatus: true, returnStdout: true, label: 'labelname')
          }
        }

        stage('Sleep') {
          steps {
            powershell(script: 'hostname', returnStdout: true, returnStatus: true)
            sleep 1
            cleanWs(cleanWhenSuccess: true, cleanWhenFailure: true, cleanWhenAborted: true, cleanWhenNotBuilt: true, cleanWhenUnstable: true, cleanupMatrixParent: true, deleteDirs: true, disableDeferredWipeout: true)
          }
        }

        stage('Hostname2') {
          steps {
            powershell(script: 'hostname', returnStdout: true)
          }
        }

      }
    }

  }
}
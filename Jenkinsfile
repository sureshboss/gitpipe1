pipeline {
  agent any
  stages {
    stage('Hostname') {
      parallel {
        stage('Hostname') {
          steps {
            step {myvar=(powershell(script: 'hostname', returnStatus: true, returnStdout: true, label: 'labelname')).trim}
          }
        }

        stage('Sleep') {
          steps {
            powershell(script: 'hostname', returnStdout: true, returnStatus: true)
            sleep 1
            echo myvar
            cleanWs(cleanWhenSuccess: true, cleanWhenFailure: true, cleanWhenAborted: true, cleanWhenNotBuilt: true, cleanWhenUnstable: true, cleanupMatrixParent: true, deleteDirs: true, disableDeferredWipeout: true)
          }
        }

        stage('Hostname2') {
          steps {
            powershell 'hostname'
          }
        }

      }
    }

    stage('Test') {
      steps {
        bat(script: 'dir', returnStdout: true, returnStatus: true)
        echo '${labelname}'
      }
    }

  }
}

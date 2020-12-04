pipeline {
  agent any
  stages {
    stage('Begin') {
      steps {
        powershell(script: '$name=$env:name;echo "hi $name how are you?"', label: 'msg', returnStatus: true, returnStdout: true)
      }
    }

    stage('print') {
      steps {
        echo '${msg}'
      }
    }

    stage('check') {
      steps {
        powershell(script: '$disk = Get-WmiObject Win32_LogicalDisk -Filter "DeviceID=\'C:\'" |  Select-Object Size,FreeSpace ;echo ((($disk.FreeSpace)/$disk.Size)*100)', returnStdout: true, returnStatus: true)
      }
    }

  }
  environment {
    name = 'suresh'
    team = 'raiseit2.0'
    dept = 'imsauto'
    servername = ''
  }
}
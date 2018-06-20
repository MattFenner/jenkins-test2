pipeline {
  agent none
  stages {
    stage('Dev') {
      agent { label 'windows' }
      steps {
        echo 'lint'
        powershell './build.ps1'
        echo 'unit test'
      }
    }
    stage('input') {
      agent none
      steps {
        input(message: 'Deploy to the Test environment?')
      }
    }
    stage('Test') {
      agent { label 'windows' }
      steps {
        echo 'deploy to test'
      }
    }
    }
  }
}
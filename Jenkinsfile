pipeline {
  agent { label 'windows' }
  stages {
    stage('Dev') {
      steps {
        echo 'lint'
        powershell './build.ps1'
        echo 'unit test'
      }
    }
    input(message: 'Deploy to the Test environment?')
    stage('Test') {
      steps {
        echo 'deploy to test'
      }
    }
    input(message: 'Deploy to the Staging environment?')
    stage('Staging') {
      steps {
        echo 'deploy to staging'
      }
    }
    input(message: 'Deploy to the Prod environment?')
    stage('Prod') {
      steps {
        echo 'deploy to prod'
      }
    }
  }
}
pipeline {
  // agent { label 'windows' }
  agent any
  stages {
    stage('Nested') {
      stages {
        stage ('1') {
          echo '1'
        }
        stage ('2') {
          echo '2'
        }
      }
    }
    stage('Dev') {
      steps {
        echo 'lint'

        // powershell 'build.ps1'
        echo 'unit test'
      }
    }
    stage('Test') {
      steps {
        input(message: 'Deploy to the Test environment?')
        echo 'deploy to test'
      }
    }
    stage('Staging') {
      steps {
        input(message: 'Deploy to the Staging environment?')
        echo 'deploy to staging'
      }
    }
    stage('Prod') {
      steps {
        input(message: 'Deploy to the Prod environment?')
        echo 'deploy to prod'
      }
    }
  }
}
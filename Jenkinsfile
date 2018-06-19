pipeline {
  agent any
  stages {
    stage('Dev') {
      steps {
        echo 'lint'
        echo 'build'
        echo 'unit test'
      }
    }
    stage('Test') {
      steps {
        input(message: 'Deploy to the Test Environment?')
        echo 'deploy to test'
      }
    }
    stage('Staging') {
      steps {
        input(message: 'Deploy to the Staging Environment?')
        echo 'deploy to staging'
      }
    }
    stage('Prod') {
      steps {
        input(message: 'Deploy to the Prod Environment?')
        echo 'deploy to prod'
      }
    }
  }
}
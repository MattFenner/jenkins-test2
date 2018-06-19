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
        echo 'deploy to test'
      }
    }
    stage('Staging') {
      steps {
        echo 'deploy to staging'
      }
    }
    stage('Prod') {
      steps {
        echo 'deploy to prod'
      }
    }
  }
}
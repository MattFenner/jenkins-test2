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
    stage('trigger test job') {
      agent none
      steps {
        echo JOB_NAME
        build(job: './SG Test/master')
      }
    }
    // stage('input') {
    //   agent none
    //   steps {
    //     timeout(time:5, unit:'DAYS') {
    //       input(message: 'Deploy to the Test environment?')
    //     }
    //   }
    // }
    // stage('Test') {
    //   agent { label 'windows' }
    //   steps {
    //     echo 'deploy to test'
    //   }
    // }
  }
}
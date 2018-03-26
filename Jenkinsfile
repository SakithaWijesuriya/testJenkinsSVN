pipeline {
  agent any
  stages {
    stage('1') {
      parallel {
        stage('1') {
          steps {
            echo '1'
          }
        }
        stage('2') {
          steps {
            bat(script: '@ECHO OFF ECHO Hello World! PAUSE', returnStatus: true, encoding: 'bye')
          }
        }
      }
    }
    stage('3') {
      steps {
        retry(count: 3) {
          echo 'n time'
        }
        
      }
    }
  }
}
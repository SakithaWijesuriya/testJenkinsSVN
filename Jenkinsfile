pipeline {
  agent any
  stages {
    stage('1') {
      steps {
        echo '1'
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
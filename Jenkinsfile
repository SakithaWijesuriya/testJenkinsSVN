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
            echo '2'
          }
        }
        stage('4') {
          steps {
            sleep 5
          }
        }
      }
    }
    stage('3') {
      parallel {
        stage('3') {
          steps {
            echo '3'
            timeout(time: 3, unit: 'SECONDS') {
              sleep 2
            }
            
          }
        }
        stage('5') {
          steps {
            retry(count: 3) {
              echo 'retry'
            }
            
          }
        }
      }
    }
    stage('6') {
      steps {
        echo '6'
      }
    }
  }
}
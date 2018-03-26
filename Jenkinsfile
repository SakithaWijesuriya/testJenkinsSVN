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
            node(label: '2') {
              echo 'node allocate'
            }
            
          }
        }
        stage('send mail') {
          steps {
            mail(subject: 'test', body: 'testbody', to: 'snwijesuriya@virtusa.com', bcc: '""', cc: '""', charset: '""', from: 'snwijesuriya@virtusa.com', mimeType: '""', replyTo: '""')
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
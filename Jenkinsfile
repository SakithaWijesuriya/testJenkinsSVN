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
            node(label: '192.168.1.19 ') {
              echo 'call pc'
            }
            
          }
        }
        stage('error') {
          steps {
            svn(url: 'C:\\Users\\snwijesuriya\\.jenkins\\workspace\\FuntionTest_master-V7SSUSIUSKLGDLSMA7EIJATZVAJMJMUU5EFWIJ3ZS55PSVMS7Q3Q', poll: true)
          }
        }
      }
    }
    stage('3') {
      parallel {
        stage('3') {
          steps {
            retry(count: 3) {
              echo 'n time'
            }
            
          }
        }
        stage('') {
          steps {
            tempoTool 'C:\\Sakitha\\apache-tomcat-8.0.50\\bin'
          }
        }
      }
    }
  }
}
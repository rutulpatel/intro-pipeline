pipeline {
  agent {
    label 'centos'
  }

  stages {
    stage('Say Hello') {
      steps {
        echo 'Hello jenkins'
      }
    }
    stage('Testing') {
      failFast true
      parallel {
        stage ('Java 8'){
          agent {
            label 'centos'
          }
          steps {
            sh 'java -version'
            sleep (time: 10, unit: 'SECONDS')
          }
        }
        
      }
    }
  }

  post {
    aborted {
      echo 'why didnt you push the button?'
    }
  }
}

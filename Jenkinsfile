pipeline {
  agent {
    docker {
      image 'golang:1.10.1-alpine'
      label 'docker'
    }
    
  }
  stages {
    stage('Say Hello') {
      steps {
        echo 'Hello jenkins'
      }
    }
    stage('Go version') {
      steps {
        sh 'go version'
      }
    }
  }
}

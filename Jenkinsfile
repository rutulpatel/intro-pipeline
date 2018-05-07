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
    stage('Java version') {
      steps {
        sh 'java -version'
      }
    }
  }
}

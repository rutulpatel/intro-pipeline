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
    stage ('Deploy') {
      input {
        message 'should we continue?'
      }
      steps {
        echo "continuing with deployment"
      }
    }
  }
}

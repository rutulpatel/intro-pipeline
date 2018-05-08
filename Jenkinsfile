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
      options {
        timeout(time: 30, unit: 'SECONDS')
      }
      input {
        message 'should we continue?'
      }
      steps {
        echo "continuing with deployment"
      }
    }
  }
}

pipeline {
  agent {
    label 'centos'
  }

  stages {
    stage('Say Hello') {
      steps {
        echo 'Hello jenkins'
        sh 'java -version'
        echo "${TEST_USER_USR}"
        echo "${TEST_USER_PSW}"
      }
    }
  }
  environment {
    MY_NAME="rutul"
    TEST_USER= credentials('admin')
  } 
  parameters {
    string(name: 'Name', defaultValue: 'Whoever you are', description: 'who should i say hi to?')
  }
}

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
        message 'Which version?'
        ok "Deploy"
        parameters {
          choice(name: 'APP_VERSION', choices: "v1.1\nv1.2\nv1.3", description: 'What to deploy?')
        }
      }
      steps {
        echo "Deploying ${APP_VERSION}."
      }
    }
  }
}

pipeline {
  agent {
    docker {
      image 'ubuntu'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'uname -a'
      }
    }
    stage('Test') {
      environment {
        CI = 'true'
      }
      steps {
        sh './jenkins/scripts/test.sh'
      }
    }
  }
}
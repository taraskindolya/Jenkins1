pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Init') {
      environment {
        CI = 'true'
      }
      steps {
        echo 'Functional tests'
      }
    }
    stage('Build') {
      steps {
        echo 'Distribute to Bintray'
      }
    }
    stage('Testing') {
      steps {
        echo 'FT'
        echo 'UT'
        echo 'VT'
      }
    }
  }
}
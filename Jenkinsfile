pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'npm install'
          }
        }
        stage('SA') {
          steps {
            echo 'Static Analysis'
          }
        }
      }
    }
    stage('FT') {
      parallel {
        stage('FT') {
          environment {
            CI = 'true'
          }
          steps {
            echo 'Functional tests'
          }
        }
        stage('UT') {
          steps {
            echo 'Unit Tests'
          }
        }
        stage('VT') {
          steps {
            echo 'Valgrind tests'
          }
        }
      }
    }
    stage('Release') {
      steps {
        echo 'Distribute to Bintray'
      }
    }
  }
}
pipeline {
  agent {
    node {
      label 'maven'
    }

  }
  stages {
    stage('test') {
      steps {
        sh '''
  npm ci
  npm test'''
      }
    }

  }
  post {
    always {
      echo 'I will always say Hello again!'
    }

  }
}
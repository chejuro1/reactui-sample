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

    stage('deploy ') {
      steps {
        sh '''oc project react-intro2
oc start-build greeting-service --follow --wait'''
      }
    }

  }
  post {
    always {
      echo 'I will always say Hello again!'
    }

  }
}
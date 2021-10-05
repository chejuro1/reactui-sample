pipeline {
  agent none
  stages {
    stage('deploy') {
      steps {
        sh ''' sh \'\'\'
            oc project react-intro2
            oc start-build greeting-service --follow --wait
    \'\'\''''
      }
    }

  }
  post {
    always {
      echo 'I will always say Hello again!'
    }

  }
}
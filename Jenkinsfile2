pipeline {
  agent none

  environment {
    MAJOR_VERSION = 1
  }

  
    stage('build') {
      agent {
        label 'apache'
      }
      steps {
        sh 'ant -f build.xml -v'
      }
  }
}

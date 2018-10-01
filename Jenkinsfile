pipeline {
  agent none

  environment {
    MAJOR_VERSION = 1
  }

  stages {
    
    stage('build') {
      agent {
        label 'Linux'
      }
      steps {
        sh 'ant -f build.xml -v'
      }
      post {
        success {
          archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
        }
    }
    
    }
  }
}

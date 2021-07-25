pipeline {
  agent {
    node {
      label 'start'
    }

  }
  stages {
    stage('paso1') {
      steps {
        sh 'npm run build'
      }
    }

    stage('error') {
      steps {
        archiveArtifacts(caseSensitive: true, onlyIfSuccessful: true, artifacts: 'a')
      }
    }

  }
  environment {
    dev = 'dev'
  }
}
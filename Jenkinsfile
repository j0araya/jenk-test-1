pipeline {
  agent any
  stages {
    stage('paso1') {
      steps {
        sh 'npm run build'
      }
    }

    stage('') {
      steps {
        archiveArtifacts(caseSensitive: true, onlyIfSuccessful: true, artifacts: 'a')
      }
    }

  }
}
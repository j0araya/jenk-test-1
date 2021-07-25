pipeline {
  agent any
  stages {

    stage('Build') {
      steps {
        echo 'Building..'
        sh 'npm run build'
      }
    }

     stage('Test') {
        steps {
            echo 'Testing..'
            sh 'npm run test'
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
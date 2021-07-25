pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
        bat(script: 'cd jenkins-app & npm run build', label: 'cd')
        bat(script: 'dir', label: 'dir')
        bat(script: 'npm run build', label: 'build')
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
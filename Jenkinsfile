pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building..'
        bat(script: 'cd jenkins-app', label: 'cd')
        bat(script: 'ls', label: 'ls')
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
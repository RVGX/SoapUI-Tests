pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/RVGX/SoapUI-Tests', branch: 'main')
      }
    }

    stage('ShellScript ls -la') {
      steps {
        sh 'ls -la'
      }
    }

  }
}
pipeline {
  agent any
  stages {
    stage('Checkout Code') {
      steps {
        git(url: 'https://github.com/RVGX/SoapUI-Tests', branch: 'dev')
      }
    }

    stage('Log ShellScript ls -la') {
      parallel {
        stage('Log ShellScript ls -la') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-End Unit Tests') {
          steps {
            sh 'cd curriculum-front && npm i && npm run test:unit'
          }
        }

      }
    }

  }
}
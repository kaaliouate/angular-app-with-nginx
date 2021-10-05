pipeline {
  agent any
  stages {
    stage("install") {
      steps {
        echo 'npm install ...'
        nodejs('NodeJS-15') {
          sh 'npm install'
        }
      }
    }

    stage('Test') {
      parallel {
        stage('Static code analysis') {
          steps {
            echo 'npm run lint ...'
            nodejs('NodeJS-15') {
              sh 'npm run lint'
            }
          }
        }
        stage('Unit tests') {
          steps {
            echo 'npm run test ...'
            nodejs('NodeJS-15') {
              sh 'npm run test'
            }
          }
        }
      }
    }

    stage("build") {
      steps {
        echo 'npm build --prod ...'
        nodejs('NodeJS-15') {
          sh 'npm run build --prod'
        }
      }
    }
  }
}
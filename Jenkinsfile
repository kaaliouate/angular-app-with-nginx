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
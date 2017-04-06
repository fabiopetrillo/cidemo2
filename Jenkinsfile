pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        parallel(
          "Compile": {
            sh './gradlew compileJava'
            
          },
          "": {
            sh 'Compiling'
            
          }
        )
      }
    }
    stage('Test') {
      steps {
        sh './gradlew test'
      }
    }
    stage('Build') {
      steps {
        sh './gradlew build'
      }
    }
    stage('Deploy') {
      steps {
        sh 'Deploy DONE!'
      }
    }
  }
}
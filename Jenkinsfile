pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        parallel(
          "Compile": {
            sh './gradlew compileJava'
            
          },
          "error": {
            echo 'Compiling'
            
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
        echo 'DONE!'
      }
    }
  }
}
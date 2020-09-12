pipeline {
  agent any
  stages {
    stage('s1') {
      steps {
        sh 'echo hello'
        sh 'echo aditya'
      }
    }

    stage('s2') {
      parallel {
        stage('s2') {
          steps {
            echo 'hello print'
          }
        }

        stage('s3') {
          steps {
            sh 'echo para'
          }
        }

      }
    }

  }
}
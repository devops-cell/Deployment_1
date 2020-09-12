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
            input(message: 'Want to proceed', id: '1', ok: 'yes', submitter: 'durgesh')
          }
        }

        stage('s3') {
          steps {
            sh 'echo para'
            input(message: 'ddd', ok: 'yes')
          }
        }

      }
    }

    stage('s4') {
      steps {
        sh 'echo hello'
      }
    }

  }
}
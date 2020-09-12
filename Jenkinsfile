pipeline {
  agent any
  stages {
    stage('Fetching Repo') {
      steps {
        sh 'echo hello'
      }
    }

    stage('DB Query') {
      steps {
        sh 'echo hello'
      }
    }

    stage('Sending result to email') {
      steps {
        mail(subject: 'Result', body: 'test', from: 'pschamp01@gmail.com', to: 'sweekrutikayarkar06@gmail.com;aditya.family0312@gmail.com;durgesh.raj@yahoo.com')
      }
    }

  }
}
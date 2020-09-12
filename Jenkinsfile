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
        mail(subject: 'Result', body: 'test', from: 'pschamp01@gmail.com', to: 'durgesh.raj@yahoo.com', bcc: 'sweekrutikayarkar06@gmail.com', cc: 'aditya.family0312@gmail.com')
      }
    }

  }
}
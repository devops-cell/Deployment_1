pipeline {
  agent any
  stages {
    stage('Fetching Repo') {
      steps {
        git 'https://github.com/devops-cell/Deployment_1.git'
      }
    }

    stage('DB Query') {
      steps {
        sh '''a=`cat query.sql`
        mysql -h productiondb.cdu93y40ni7m.us-east-1.rds.amazonaws.com -u admin -paditya.kumar -e "use RealParsmodel; $a" > test.html
        '''
      }
    }

    stage('Sending result to email') {
      steps {
        sh '''b=`cat test.html`
          '''
        mail(subject: 'Result',emailext mimeType: 'text/html', body: ${FILE, path="test.html"}, from: 'pschamp01@gmail.com', to: 'durgesh.raj@yahoo.com', bcc: 'sweekrutikayarkar06@gmail.com', cc: 'aditya.family0312@gmail.com')
      }
    }

  }
}

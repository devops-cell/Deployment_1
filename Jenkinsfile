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
        mail(subject: 'Result', mimeType: 'text', to: 'pshamp01@gmail.com', from: 'pschamp01@gmail.com', body: 'test')
      }
    }

  }
}

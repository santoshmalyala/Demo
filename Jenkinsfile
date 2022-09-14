pipeline {
  agent any
  stages {
    stage('Install apache') {
      steps {
        sh 'sudo yum install httpd -y'
      }
    }

    stage('start the service') {
      steps {
        sh 'sudo service httpd restart'
      }
    }

    stage('Pull the code from Git') {
      steps {
        git(url: 'https://github.com/santoshmalyala/Demo.git', branch: 'main')
      }
    }

    stage('To copy to var folder') {
      steps {
        sh 'sudo cp  -R * /var/www/html'
      }
    }

  }
}
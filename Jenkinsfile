pipeline {
  agent any
  stages {
    stage('Fetching Code') {
      steps {
        git(url: 'https://github.com/SaiSindhuManne/jenkins.git', branch: 'main')
      }
    }

    stage('Install Server') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Deploy Application') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}
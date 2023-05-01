pipeline {
  agent any
  stages {
    stage('Fetch code') {
      steps {
        git(url: 'https://github.com/gops7066/pipe.git', branch: 'main')
      }
    }

    stage('install apache') {
      steps {
        sh 'sudo apt install apache2 -y '
      }
    }

    stage('deploy app') {
      steps {
        sh 'sudo cp -r * /var/www/html/'
      }
    }

  }
}
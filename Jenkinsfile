pipeline {
  agent any
  stages {
    stage ('Fetch code') {
      steps {
        git branch: 'main', url: 'https://github.com/krsharathrao/jenkins-demo.git'
      }
    }
    stage ('Install & start apache') {
      steps {
        sh '''sudo apt install -y apache2
              sudo service start apache2'''
      }
    }
    stage ('config apache') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }
  }
}

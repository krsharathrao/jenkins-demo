pipeline {
  agent any
    stages {
        stage ('Fetch code') {
          steps {
            git branch: 'main', url: 'https://github.com/krsharathrao/jenkins-demo.git'
          }
        }
        stage ('Install apache') {
          steps {
            sh 'sudo apt install apache2 -y'
          }
        }
        stage ('Deploy app') {
          steps {
            sh 'sudo cp -R * /var/www/html/'
          }
        }
    }
}

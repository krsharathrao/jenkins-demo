pipeline {
  agent any
  stages {
    stage {
      step ('Fetch code') {
        git branch: 'main', url: 'https://github.com/krsharathrao/jenkins-demo.git'
      }
    }
    stage {
      step ('Install & start apache') {
        sh '''sudo apt install -y apache2
              sudo service start apache2'''
      }
    }
    stage {
      step ('config apache') {
        step 'sudo cp -R * /var/www/html/'
      }
    }
  }
}

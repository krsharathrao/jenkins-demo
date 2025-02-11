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
                sh '''sudo apt install -y apache2
                      sudo service apache2 start'''
            }
        }
        stage ('deploy app') {
            steps {
                sh 'sudo cp -R * /var/www/html/'
            }
        }
        
    }
    
}

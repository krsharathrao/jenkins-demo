pipeline {
    agent any
    stages {
        stage ('Fetch code') {
            steps {
                git branch: 'main', url: 'https://github.com/krsharathrao/jenkins-demo.git'
            }
        }
        stage ('remove apache') {
            steps {
                sh 'sudo apt remove -y apache2'
            }
        }
        
    }
    
}

pipeline {
    agent any
    stages {
        stage('Get code from github') {
            steps {
              git branch: 'main', url: 'https://github.com/fullstackjava082023/HW1Jenkins.git'
            }
        }
        stage('Run') {
            steps {
               sh 'python3 main.py'
            }
        }
        
    }
}

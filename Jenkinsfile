pipeline {
    agent any
    parameters {
        booleanParam(defaultValue: false, description: 'dry run?', name: 'DRY_RUN')
    }
    stages {
        stage('Get code from github') {
            steps {
              git branch: 'main', url: 'https://github.com/fullstackjava082023/HW1Jenkins.git'
            }
        }
        stage('Run') {
            when {
                expression { params.DRY_RUN == false }
            }
            steps {
               sh 'python3 main.py > output.txt'
            }
        }        
    }
}

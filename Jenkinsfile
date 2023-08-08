pipeline {
    agent any
    
    tools {
        go '1.19'
    }
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout your code from version control
                checkout scm
            }
        }
       
        stage('Test') {
            steps {
                sh 'go mod init helloworld'
                sh 'go test'
            }
        }
        
        stage('Build') {
            steps {
                sh 'go build -o myapp'
                sh './myapp'
            }
        }
    }
}
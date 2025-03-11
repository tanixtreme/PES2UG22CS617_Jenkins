pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                
                build 'PES2UG22C'
                
                
                sh 'g++ -o output min.cpp'
            }
        }
        
        stage('Test') {
            steps {
                
                sh './output'
            }
        }
        
        stage('Deploy') {
            steps {
                
                echo 'Deployment completed successfully'
            }
        }
    }
    
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}

pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                // This builds a Jenkins job with your SRN identifier
                build 'PES2UG22CS617-1'
                
                // Compile your C++ file
                sh 'g++ -o output main.cpp'
            }
        }
        
        stage('Test') {
            steps {
                // Run the compiled program to display output
                sh './output'
            }
        }
        
        stage('Deploy') {
            steps {
                // Simple deploy message (placeholder for actual deployment)
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

pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o pipeline_file_PES1UG20CS054 pipeline_file_PES1UG20CS054.cpp'
                build job: 'PES1UG20CS054-1'
            }
        }
        
        stage('Test') {
            steps {
                sh './pipeline_file_PES1UG20CS054'
            }
        }
        
        stage('Deploy') {
            steps {
                'Deployment'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
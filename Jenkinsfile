pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o your_program PES1UG21CS744-4.cpp'
            }
            post {
                always {
                    script {
                        echo 'Build stage completed'
                    }
                }
            }
        }
        
        stage('Test') {
            steps {
                sh './your_program'
            }
            post {
                always {
                    script {
                        echo 'Test stage completed'
                    }
                }
            }
        }
        
        stage('Deploy') {
            steps {
                // Add deployment steps here if needed
            }
            post {
                always {
                    script {
                        echo 'Deploy stage completed'
                    }
                }
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

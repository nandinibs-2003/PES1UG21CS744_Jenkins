pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output PES1UG21CS744-1.cpp'
                    echo 'Build Stage Successful'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './output'
                    echo 'Test Stage Successful'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment not required for this pipeline'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
        success {
            echo 'Pipeline succeeded'
        }
        always {
            echo 'Pipeline completed'
        }
    }
}




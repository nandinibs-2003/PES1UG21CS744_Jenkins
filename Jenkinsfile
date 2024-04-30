pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output PES1UG21CS744.cpp'
                    echo 'Build Stage Successful'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Intentional error: Trying to execute a non-existing script
                    sh './non_existing_script.sh'
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



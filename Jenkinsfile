pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ main.cpp -o PES1UG22AM115-1'
            }
        }
        stage('Test') {
            steps {
                    // Intentional error
                    sh './PES1UG22AM115-1_hello'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

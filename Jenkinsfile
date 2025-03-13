pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    build 'PES1UG22CS190-1'
                    sh 'g++ -o main.cpp -o output'
                }
            }
        }

        stage('Test') {
            steps {
                  sh './output'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add deployment commands here
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}

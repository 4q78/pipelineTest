pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                script {
                    // Clone the repository
                    git url: 'https://github.com/4q78/pipelineTest', branch: 'main'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Compile your code
                    sh 'javac pipeline.java'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run your tests
                    sh 'java pipeline'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Deploy your application
                    echo 'Deploying application...'
                }
            }
        }
    }

    post {
        always {
            script {
                // Clean up after build
                echo 'Cleaning up...'
            }
        }
    }
}
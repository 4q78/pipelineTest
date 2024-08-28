pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                // Clone the repository
                git 'https://github.com/4q78/pipelineTest'
            }
        }

        stage('Build') {
            steps {
                // Compile your code
                sh 'javac HelloWorld.java'
            }
        }

        stage('Test') {
            steps {
                // Run your tests
                sh 'java HelloWorld'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy your application (this can be as simple as an echo in this demo)
                echo 'Deploying application...'
            }
        }
    }

    post {
        always {
            // Clean up after build
            echo 'Cleaning up...'
        }
    }
}

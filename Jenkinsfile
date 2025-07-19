pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
                checkout scm
            }
        }

        stage('Parallel Quality Checks') {
            parallel {
                stage('Lint') {
                    steps {
                        echo 'Running lint check...'
                        sh 'echo "flake8 app/"'
                    }
                }

                stage('Unit Tests') {
                    steps {
                        echo 'Running unit tests...'
                        sh 'echo "pytest tests/"'
                    }
                }

                stage('Security Scan') {
                    steps {
                        echo 'Running security scan...'
                        sh 'echo "trivy scan simulation..."'
                    }
                }
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                sh 'echo "Simulate docker build/app packaging..."'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh 'echo "Simulate deployment..."'
            }
        }
    }
}

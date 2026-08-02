pipeline {
    agent any

    environment {
        IMAGE_NAME = "tummapragna/sample-app"
    }

    stages {
        stage('Clone') {
            steps {
                echo 'Repository cloned'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh '''
                whoami
                docker build -t $IMAGE_NAME .
                '''
            }
        }

        stage('Push Docker Image') {
            steps {
                echo 'Docker image build completed'
            }
        }
    }

    post {
        always {
            echo 'Pipeline Finished'
        }
    }
}

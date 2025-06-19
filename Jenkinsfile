pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/kusuma-1004/aws_pipeline.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t python-ci-cd-app .'
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    sh 'docker rm -f python-ci-cd-app || true'
                    sh 'docker run -d -p 5000:5000 --name python-ci-cd-app python-ci-cd-app'
                }
            }
        }
    }

    post {
        always {
            echo "Pipeline execution finished."
        }
    }
}

pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Build Docker image
                    docker.build("my-docker-image:${env.BUILD_ID}")
                }
            }
        }
        stage('Deploy to Local Docker') {
            steps {
                script {
                    // Deploy Docker image to local Docker
                    docker.image("my-docker-image:${env.BUILD_ID}").run('-p 8080:80')
                }
            }
        }
    }
}

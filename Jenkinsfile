pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout scm
                }
            }
        }

        stage('Build and Push Docker Image') {
            steps {
                script {
                    // Define your Docker image name
                    def dockerImage = 'snehal01102002/your-docker-repo:latest'

                    // Build and tag the Docker image
                    docker.build(dockerImage)

                    // Push the Docker image to the registry
                    docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials-id') {
                        docker.image(dockerImage).push()
                    }
                }
            }
        }
    }
}

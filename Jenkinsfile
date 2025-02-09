pipeline {
    agent any
    environment {
        DOCKER_IMAGE = 'myjenkins-blueocean:latest'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the Docker image on localhost...'
                script {
                    docker.build(DOCKER_IMAGE)
                }
            }
        }
    }
}

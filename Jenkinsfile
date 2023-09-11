pipeline {
    agent any

   

    stages {
        stage('Build Docker Image') {
            steps {
               dir('react-ssr/') {
                script {
                    sh ' sudo docker build -t shankar123321/react-ssr- . '
                }
               }
            }
        }

        stage('docker run') {
            steps {
               dir('react-ssr/') {
                script {
                    // Run the Docker container from the built image
                    sh ' sudo docker run -d -p 2048:2048 shankar123321/react-ssr-:latest '
                }
               }
            }
        }
    }

    post {
        success {
            // Notify or perform actions when the pipeline succeeds
        }
        failure {
            // Notify or perform actions when the pipeline fails
        }
    }
}

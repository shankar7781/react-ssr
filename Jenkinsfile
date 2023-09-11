pipeline {
    agent any

   

    stages {
        stage('Build Docker Image') {
            steps {
               
                script {
                    sh '  docker build -t shankar123321/react-ssr . '
                    sh ' pwd '
               
               }
            }
        }

        stage('docker run') {
            steps {
               
                script {
                    // Run the Docker container from the built image
                     sh '  docker run -d -p 2048:2048 shankar123321/react-ssr:latest '
                    sh ' echo "test" '
               
               }
            }
        }
    }

    post {
        success {
            // Notify or perform actions when the pipeline succeeds
            sh ' echo "success" '
         }
        failure {
            // Notify or perform actions when the pipeline fails
             sh ' echo "failed" '
        }
    }
}
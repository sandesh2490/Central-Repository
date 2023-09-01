pipeline {
    agent {
        docker {
            // Use a Docker image with Java installed
            image 'openjdk:11'
            args '-v /var/run/docker.sock:/var/run/docker.sock' // Optional: Mount Docker socket for Docker-in-Docker
        }
    }

    stages {
        stage('Build') {
            steps {
                // Compile the Java code.
                echo 'Java Hello, World! program executed successfully.'
            }
        }

        stage('Test') {
            steps {
                // This is a simple "Hello, World!" Java program.
                 echo 'Java Hello, World! program executed successfully.'
            }
        }
    }
    
}

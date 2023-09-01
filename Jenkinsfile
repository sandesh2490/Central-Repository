pipeline {
    agent {
        docker {
            // Use a Docker image with Java installed
            image 'openjdk:11'
            args '-v /var/run/docker.sock:/var/run/docker.sock' // Optional: Mount Docker socket for Docker-in-Docker
        }
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code repository (e.g., Git).
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Compile the Java code.
                sh 'javac HelloWorld.java'
            }
        }

        stage('Test') {
            steps {
                // This is a simple "Hello, World!" Java program.
                sh 'java HelloWorld'
            }
        }
    }
    
    post {
        success {
            // This block is executed if the pipeline succeeds.
            echo 'Java Hello, World! program executed successfully.'
        }
        failure {
            // This block is executed if the pipeline fails.
            echo 'Java Hello, World! program execution failed.'
        }
    }
}

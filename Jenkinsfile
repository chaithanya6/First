pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Print the JDK version
                sh 'java -version'
                // Compile the Java program
                sh 'javac Hello.java'
            }
        }

        stage('Test') {
            steps {
                // Run the Java program
                sh 'java Hello'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add deployment steps here if any
            }
        }
    }

    post {
        always {
            // Clean up workspace
            cleanWs()
        }
    }
}

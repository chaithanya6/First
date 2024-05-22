pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the Git repository
                git url: 'https://github.com/chaithanya6/First.git', branch: 'main'
            }
        }

        stage('Build') {
            steps {
                // Print the JDK version
                bat 'java -version'
                // Compile the Java program
                bat 'javac Hello.java'
            }
        }

        stage('Test') {
            steps {
                // Run the Java program
                bat 'java Hello'
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

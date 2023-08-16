pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your code from the version control system
                // For example, if you're using Git:
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Build your project using Maven
                sh 'mvn clean compile'
            }
        }

        stage('Unit Tests') {
            steps {
                // Run JUnit tests using Maven
                sh 'mvn test'
            }
        }
    }

    post {
        always {
            // Archive test reports
            junit '**/target/surefire-reports/*.xml'
        }
    }
}


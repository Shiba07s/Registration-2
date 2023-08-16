pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout your source code from version control
                checkout scm
            }
        }

      stages {
        stage('Build') {
            steps {
                git 'https://github.com/LdKishan/Registration-2.git'
              sh './mvnw clean compile'
            }
        }

         stages {
        stage('Test') {
            steps {
                
              sh './mvnw test'
              //bat '.\mvnw test'
            }
        }
      

        post('Unit Tests') {
            steps {
                // Set up your environment, install dependencies, etc.
                sh 'maven install' // Example: Installing npm dependencies

                // Run your unit tests
                sh 'maven test' // Example: Running unit tests using npm

                // Archive test results for later viewing in Jenkins
                junit 'git 'https://github.com/LdKishan/Registration-2.git'                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      ' // Example: JUnit test report
            }
        }

        // Add more stages for other pipeline steps (e.g., build, deploy, etc.)
    }
}

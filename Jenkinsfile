pipeline {
    agent any
    tools {
       maven 'maven-3.6.3' 
        }
    stages {
        stage('Checkout') {
            steps {
                // Check out your source code from your version control system (e.g., Git)
                checkout scm
            }
        }

        stage('Unit Test') {
            steps {
                // Run Maven using the configured version
                sh 'mvn clean test'
            }
        }

        // (Other stages...)

        stage('Build') {
            steps {
                // Build the source code using Maven
                sh 'mvn clean package'
            }
        }
    }
}

pipeline {
    agent any

    // Define environment variables for Maven
    environment {
        MAVEN_HOME = tool 'Maven 3.9.4' // Name of the Maven tool defined in Jenkins
        PATH = "$MAVEN_HOME/bin:$PATH"
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

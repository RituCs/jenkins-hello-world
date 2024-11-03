pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage('Echo Version') {
            steps {
                sh 'echo Print Maven version'
                sh 'mvn -v'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package -DskipTests=true'
            }
        }
         stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}


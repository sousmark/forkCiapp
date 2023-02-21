pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                .\mvnw clean package
            }
        }
        stage('Test') {
            steps {
                .\mvnw test
            }
        }
        stage('Deploy') {
            steps {
                java -jar target/ciapp-0.0.1-SNAPSHOT.jar
            }
        }
    }
}

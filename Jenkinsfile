pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh './mvnw compile'
            }       
        }
        stage('Test') {
            steps {
                sh './mvnw test'
            }
        }
        stage('Deploy') {
            steps {
                sh './mvnw clean package'
                sh 'java -jar target/ciapp-0.0.1-SNAPSHOT.jar'
            }
        }
    }
}

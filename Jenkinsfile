pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'mvn compile'
            }       
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mvn clean package'
                sh 'java -jar target/ciapp-0.0.1-SNAPSHOT.jar'
            }
        }
    }
}

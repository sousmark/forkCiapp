pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
		echo 'Compiling...'
                sh 'sudo mvn compile'
            }       
        }
        stage('Test') {
            steps {
		echo 'Testing...'
                sh 'sudo mvn test'
            }
        }
        stage('Deploy') {
            steps {
		echo 'Deploying...'
                sh 'sudo mvn clean package'
            }
        }
    }
}

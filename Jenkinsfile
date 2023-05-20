pipeline {
    agent any
    tools{
        maven 'maven-3.9.2'
    }
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/D21IT185BapodraRajSatish/CLDC.git'
            }
        }
        
        stage('Build') {
            steps {
                sh 'mvn clean build'
            }
        }
        
        stage('Unit Tests') {
            steps {
                sh 'mvn test'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'mvn deploy'
            }
        }
    }
}

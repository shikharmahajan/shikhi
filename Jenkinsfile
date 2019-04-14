pipeline {
    agent any
    tools {
        maven 'localmaven'
        jdk 'jdk1.9'
    }
    stages {
        stage('build') {
            steps {
                echo "Building a maven project........!"
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
                echo "Testing........!"
                sh 'mvn test'
            }
        }
        stage('Clean up') {
            steps {
                echo "Cleaning up........!"
                cleanWs()
            }
        }
        
    }
}

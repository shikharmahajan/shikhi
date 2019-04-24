pipeline {
    agent any
    
parameters {
        string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
    }
tools {
        maven 'Maven'
        jdk 'JDK'
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
      stage('Example') {
            steps {
                echo "${params.Greeting} World!"
            }
        }
        
    }
}

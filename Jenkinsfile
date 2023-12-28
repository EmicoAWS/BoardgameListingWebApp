pipeline {
    agent any
    
    tools {
        jdk 'jdk11a'
        maven 'maven3a'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git 'https://github.com/emicoaws/BoardgameListingWebApp.git'
            }
        }
        
        stage('Compile') {
            steps {
               sh "mvn compile"
            }
        }
        
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
        
        stage('Package') {
            steps {
                sh "mvn package"
            }
        }
        
        stage('Install') {
            steps {
                sh "mvn install"
            }
        }
    }
}

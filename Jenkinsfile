pipeline {
    agent any
    
    tools{
        jdk 'jdk11'
        maven 'maven3'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/sniperwolf46/Petclinic.git'
            }
        }
        
        stage('compile') {
            steps {
                sh "mvn clean compile"
            }
        }
        
        stage('build') {
            steps {
                sh "mvn clean package"
            }
        }
        
        
        
    }
}

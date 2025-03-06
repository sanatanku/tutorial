pipeline {
    agent any
    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/sanatanku/tutorial.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
               sh 'ansible-playbook deploy.yml'
           }
       }
    }
} 


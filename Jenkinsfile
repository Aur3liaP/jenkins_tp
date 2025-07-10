pipeline {
    agent any

    tools {
      maven 'Maven'
    }

    stages {
        stage('Maven build') {
            steps {
                echo 'Building'
                bat 'mvn clean install'
            }
        }

        stage('Execute') {
            steps {
                echo 'Executer application'
                bat 'java -jar target/*.jar'
            }
        }
    }
}
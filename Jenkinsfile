pipeline {
    agent any

    stages {
        stage('Maven build') {
            steps {
                echo 'Building with Maven...'
                bat 'mvn clean install'
            }
        }

        stage('Execute') {
            steps {
                echo 'Running application...'
                bat 'java -jar target/*.jar'
            }
        }
    }
}
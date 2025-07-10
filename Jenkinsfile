pipeline {
    agent any

    tools {
      maven 'Maven'
    }

    stages {
        stage('Maven build') {
            steps {
                echo 'Building'
                bat 'mvn clean package'
            }
        }

        stage('Execute') {
            steps {
                echo 'Executer application'
                bat 'java -Dspring.application.exit-on-failure=true -jar target\\jenkins_tp-0.0.1-SNAPSHOT.jar'

            }
        }
    }
}
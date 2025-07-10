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
            timeout(time: 10, unit: 'SECONDS') {
                echo 'Executer application'
                bat 'start /b java -jar target\\jenkins_tp-0.0.1-SNAPSHOT.jar'
            }
            }
        }
    }
}
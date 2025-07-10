pipeline {
    agent any

    tools {
        maven 'Maven'
        jdk 'JDK'
    }

    stages {
        stage('Clone sources') {
            steps {
                echo 'Clone Repo'
                git url: 'https://github.com/Aur3liaP/jenkins_tp'
            }
        }

        stage('Maven build') {
            steps {
                echo 'Building'
                bat 'mvn clean install'
            }
        }

        stage('Execute') {
            steps {
                echo 'Execution'
                bat 'java -jar target/*.jar'
            }
        }
    }

    post {
        success {
            echo 'Build complété!'
        }
        failure {
            echo 'Build failed! :('
        }
    }
}
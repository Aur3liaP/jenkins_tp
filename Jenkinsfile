pipeline {
    agent any

    tools {
        maven 'Maven'
        jdk 'JDK'
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
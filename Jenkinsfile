pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    environment {
        SONAR_TOKEN = 'true'
    }
    stages {
        stage('Clean') {
            steps{
                echo "------------>Clean<------------"
                bat 'gradlew clean'
            }
        }

        stage('Build') {
            steps{
                echo "------------>Build<------------"
                bat 'gradlew build -x test'
            }
        }

        stage('Test') {
            steps{
                echo "------------>Build<------------"
                bat 'gradlew test'
            }
        }

        stage('Jacoco') {
            steps{
                echo "------------>Build<------------"
                bat 'gradlew jacocoTestReport'
            }
        }

        stage('Sonar') {
            steps{
                echo env.SONAR_TOKEN
            }
        }

    }
}
pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
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
    }
}
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
    }
}
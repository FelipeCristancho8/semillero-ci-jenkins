pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('Compile') {
            steps{
                echo "------------>Compile<------------"
                bat 'gradle build'
            }
        }
    }
}
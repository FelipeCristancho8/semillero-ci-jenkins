pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        stage('Compile & Unit Tests') {
            steps{
                echo "------------>Compile & Unit Tests<------------"
                sh 'gradle --b ./build.gradle test'
            }
        }
    }
}
pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    stages {
        steps{
            echo "------------>Compile & Unit Tests<------------"
        	sh 'gradle --b ./build.gradle test'
        }
    }
}
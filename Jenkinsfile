pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }

    stage('Compile & Unit Tests') {
          steps{
              echo "------------>Compile & Unit Tests<------------"
              sh 'gradle --b ./build.gradle test'
          }
    }
}
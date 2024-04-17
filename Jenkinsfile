pipeline {
  agent any
  stages{
      stage("build"){
          steps{
              echo 'build the application'
              sh 'mvn compile'
          }
      }
      stage("test"){
          steps{
              echo 'test the application'
              sh 'mvn test'
          }
      }
      stage("package"){
          steps{
              echo 'package the application'
              sh 'mvn package -DskipTests'
          }
      }
  }

  post{
    always{
        echo 'This pipeline is completed..'
    }
  }
}

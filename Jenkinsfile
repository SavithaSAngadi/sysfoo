pipeline {
  agent {
    docker {
      image 'maven:3.6.3-jdk-11-slim'
    }

  }
  stages {
    stage('build') {
      steps {
        echo 'build the application'
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        echo 'test the application'
        sh 'mvn test'
      }
    }

    stage('package') {
      steps {
        echo 'package the application'
        sh 'mvn package -DskipTests'
      }
    }

  }
  post {
    always {
      echo 'This pipeline is completed..'
    }

  }
}
pipeline {
  agent any
  stages {
    stage('Git Pull') {
      steps {
        git 'https://github.com/ranjit-gill/samplewebapp.git'
      }
    }

    stage('Build') {
      steps {
        sh 'mvn clean install'
      }
    }

  }
}
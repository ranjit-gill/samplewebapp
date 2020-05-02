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
        sh '\'/prod/apps/apache-maven-3.6.3/bin/mvn clean install\''
      }
    }

  }
}
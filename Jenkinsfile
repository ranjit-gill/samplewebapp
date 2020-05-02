pipeline {
  agent any
  stages {
    stage('Fetch Code') {
      steps {
        git 'https://github.com/ranjit-gill/samplewebapp.git'
      }
    }

    stage('initialize ') {
      steps {
        sh '''M2_HOME=/prod/apps/apache-maven-3.6.3
export PATH=$PATH:$M2_HOME/bin
echo $PATH
mvn -version'''
      }
    }

  }
}
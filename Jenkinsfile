pipeline {
  agent any
  stages {
    stage('scm') {
      steps {
        git 'https://github.com/ranjit-gill/samplewebapp'
      }
    }

    stage('initialize') {
      steps {
        sh '''echo "PATH = ${PATH}"
echo "M2_HOME = ${M2_HOME}"
'''
      }
    }

    stage('build') {
      steps {
        sh 'mvn clean install'
      }
    }

  }
  environment {
    jdk = 'jdk8'
    maven = 'Maven 3.6.3'
  }
}
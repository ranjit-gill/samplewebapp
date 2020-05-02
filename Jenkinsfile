pipeline {
  agent any
  stages {
    stage('fetch Code') {
      steps {
        git 'https://github.com/ranjit-gill/samplewebapp.git'
        echo 'source code is fetched from GitHub'
      }
    }

    stage('build') {
      steps {
        echo 'Starting the Build Process'
        sh 'mvn clean install'
        echo 'Build Created Successfully'
      }
    }

    stage('undeploy') {
      steps {
        echo 'Undeploying existing application from tomcat'
        sh 'sudo rm -rf /usr/share/tomcat/webapps/*.war'
        sleep 30
        echo 'Application is undeployed'
      }
    }

    stage('deployment') {
      steps {
        echo 'Starting Application Deployment'
        sh 'sudo cp target/*.war /usr/share/tomcat/webapps/'
        echo 'Application Deployed Successfully'
      }
    }

  }
}
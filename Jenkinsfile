pipeline {
  agent node1
  stages {
    stage('Latest revision from SCM') {
      steps {
        git 'https://github.com/ranjit-gill/samplewebapp.git'
        echo 'source code is fetched from GitHub'
      }
    }

    stage('Builing Source Code') {
      steps {
        echo 'Starting the Build Process'
        sh 'mvn clean install'
        echo 'Build Created Successfully'
      }
    }

  }
}

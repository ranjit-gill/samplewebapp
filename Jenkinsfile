pipeline {
  agent { node { label 'linux-node-1' } }
    
	stage('Builing Source Code') {
      steps {
        echo 'Starting the Build Process'
        sh 'mvn clean install'
        echo 'Build Created Successfully'
      }
    }
    
    stage('Deploy - Staging') {
       steps {
          echo 'this will be deployed to staging'
        }
    }

    stage('Deploy - Production') {
       steps {
          echo 'this will be deployed to production'
        }
    }
}

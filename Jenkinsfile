pipeline {
  agent {
    docker {
      image 'node:latest'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Deliver') {
      steps {
        sh 'cd /var/jenkins_home/workspace/cccSmartbrainBackend_master'
        sh 'node index.js'
      }
    }
  }
  environment {
    CI = 'true'
  }
}
pipeline {
  agent any
  stages {
    stage('prepare') {
      steps {
        git(poll: true, url: 'https://github.com/happ-in/jenkinsTest.git', branch: 'main')
      }
    }

    stage('build') {
      steps {
        sh 'cd jenkinsTest/test/'
        sh 'npm install'
        sh 'npm run serve'
        sh 'npm run build'
      }
    }

  }
  tools {
    nodejs 'jenkins-node'
  }
}
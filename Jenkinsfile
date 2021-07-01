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
        sh 'ls -a'
        sh 'cd test/'
        sh 'ls -a'
        sh 'npm run build'
        sh 'npm install'
        sh 'npm run serve'
      }
    }

  }
  tools {
    nodejs 'jenkins-node'
  }
}
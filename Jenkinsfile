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
        dir('test') {  
          sh 'npm run build'
          sh 'npm install'
          sh 'npm run serve'
        }
      }
    }

  }
  tools {
    nodejs 'jenkins-node'
  }
}

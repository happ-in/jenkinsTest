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
        sh '''sh \'cd jenkinsTest\'
sh \'npm install && npm run build\''''
      }
    }

  }
}
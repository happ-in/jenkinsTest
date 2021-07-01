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
        sh '''sh \'cd /var/jenkins_home/workspace/jenkinsTest_main\'
sh \'npm install && npm run build\''''
      }
    }

  }
}
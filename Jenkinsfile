pipeline {
  agent any
  environment {
    branch = 'master'
    credentialsId: 'e093b464-4f98-4ab6-bb93-e3cacac7221f'
    scmUrl = 'https://github.com/serdarayalp/git.git'
  }
  stages {
    stage('checkout git') {
      steps {
        git branch: branch, url: scmUrl
      }
    }

    stage('build') {
      steps {
        sh 'javac HelloWorld.java'
        sh 'java HelloWorld'
      }
    }
  }
}
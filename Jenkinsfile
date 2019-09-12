pipeline {
  agent any
  environment {
    branch = 'master'
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
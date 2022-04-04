pipeline {
  agent any
  stages {
    stage('prepare') {
      steps {
        git(url: 'https://github.com/laeti33/JavaJunitWar2.git', branch: 'master')
      }
    }

    stage('build') {
      steps {
        sh 'mvn clean install'
      }
    }

    stage('test') {
      steps {
        sh 'echo \'?\''
      }
    }

    stage('deploy') {
      steps {
        sh 'echo \'deploy\''
      }
    }

  }
}
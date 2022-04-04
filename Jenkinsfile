pipeline {
  agent any
  stages {
    stage('prepare') {
      steps {
        git(url: 'https://github.com/laeti33/JavaJunitWar2/JavaJunitWar.git', branch: 'master')
      }
    }

    stage('build') {
      steps {
        sh 'mvn -v'
        sh 'mvn clean install'
      }
    }

    stage('test') {
      steps {
        junit '/surefire-reports/TEST-*.xml'
      }
    }

    stage('deploy') {
      steps {
        sh 'echo \'deploy\''
        sh 'cp target/*war/ /var/lib/tomcat9/webapps/'
      }
    }

  }
}
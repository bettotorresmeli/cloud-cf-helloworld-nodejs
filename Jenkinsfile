pipeline {
  agent any
  stages {
    stage('prepare') {
      steps {
        checkout scm
        sh '''cf login -a  https://api.cf.us10-001.hana.ondemand.com -u btorres16@gmail.com -p $CF_PASSWORD

'''
      }
    }

    stage('build') {
      steps {
        sh ''' npm install

'''
      }
    }

    stage('deploy') {
      steps {
        sh '''cf push

'''
      }
    }

  }
}
pipeline {
  agent any
  stages {
    stage('prepare') {
      steps {
        sh 'npm install -g mbt '
        checkout scm
        setupCommonPipelineEnvironment(script: this)
      }
    }

    stage('build') {
      steps {
        mtaBuild(script: this)
      }
    }

    stage('deploy') {
      steps {
        cloudFoundryDeploy(script: this)
      }
    }

  }
}
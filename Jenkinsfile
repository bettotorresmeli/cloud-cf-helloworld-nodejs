pipeline {
  agent any
  stages {
    stage('prepare') {
      steps {
        checkout scm
        setupCommonPipelineEnvironment(script: this)
      }
    }

    stage('build') {
      steps {
        mtaBuild(script: this)
      }
    }

  }
}
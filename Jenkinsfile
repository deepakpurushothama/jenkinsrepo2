pipeline {
  agent any
  stages {
    stage('Stage 1') {
      steps {
        git(url: 'https://github.com/deepakpurushothama/jenkinsrepo2', branch: 'main', credentialsId: 'a50ec051-909a-48e4-b9e6-e4997a73fcf5')
      }
    }

    stage('Stage 2 A') {
      parallel {
        stage('Stage 2 A') {
          steps {
            sh '''#!/bin/sh
echo "Stage 2A Parallel Step"'''
          }
        }

        stage('Stage 2 B') {
          steps {
            sh '''#!/bin/sh
echo "Stage 2 B Parallel step execution"'''
          }
        }

      }
    }

    stage('Stage 3') {
      steps {
        sh '''#!/bin/sh
echo "Stage 3"'''
      }
    }

  }
}

pipeline {
  agent any
  stages {
    stage('compile code') {
      steps {
        sh 'mvn compile'
      }
    }

    stage('review code') {
      steps {
        sh 'mvn -P matrix pmd:pmd'
      }
    }

    stage('test code') {
      steps {
        sh 'mvn test'
      }
    }

  }
}
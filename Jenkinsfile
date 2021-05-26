
pipeline {
  agent any
  
  stages {
    stage('requirements') {
      steps {
        sh 'gem sinatra'
      }
    }
    stage('build') {
      steps {
        sh 'bundle install'
      }
    }
    stage('test') {
      steps {
        sh 'rake ci:all'
      } 
      post {
        always {
          junit 'test/reports/TEST-AppTest.xml'
        }
      }
    }
  }
}

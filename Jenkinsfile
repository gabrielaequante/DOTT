
pipeline {
  agent any
  
  stages {
    stage('requirements') {
      steps {
        sh 'gem install bundler -v 2.2.18'
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

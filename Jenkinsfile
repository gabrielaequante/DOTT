pipeline {
    agent any

    stages {
        

        stage('SonarQube analysis') {
          environment {
              scannerHome= tool 'sonar_scanner'
            
            }
          steps {
            withSonarQubeEnv('sonar_scanner') {
              sh "${scannerHome}/bin/sonar-scanner"
        }
    }
}
    }
}

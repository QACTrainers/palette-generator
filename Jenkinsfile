pipeline {
    agent any
     stages {
         stage('install dependencies') {
            steps {
                sh 'bash scripts/install.sh'
            }
         }
        stage('Test') {
            steps {
                sh 'bash scripts/test.sh'
            }
        }
        stage('deploy') {
            steps {
                sh 'bash scripts/deploy.sh'
            }
        }
     }
            post {
        always {
            junit 'junit/test-results.xml'
            cobertura coberturaReportFile: 'coverage.xml', failNoReports: false
        }

            }
     

}
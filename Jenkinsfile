pipeline {
    agent any
    environment {
    }

     stages {
        stage('Test') {
            steps {
                sh 'bash jenkins/milestone-project/palette-generator/script/test.sh'
            }
         stages {
        stage('Run') {
            steps {
                sh 'bash jenkins/milestone-project/palette-generator/script/run.sh'
            }
            stage('Push') {
            steps {
                sh 'docker push lisaf/milestone-project:latest'
            }
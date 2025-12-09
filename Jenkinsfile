pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/RareBreedxx/git-practice.git', branch: 'main'
            }
        }

        stage('Run System Check') {
            steps {
                sh 'chmod +x system_check.sh'
                sh './system_check.sh'
            }
        }

        stage('Archive Logs') {
            steps {
                archiveArtifacts artifacts: 'system_check.log', fingerprint: true
            }
        }

     

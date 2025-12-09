pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/RareBreedxx/git-practice'
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
                archiveArtifacts artifacts: 'system_check.log', allowEmptyArchive: true
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-first-image ./docker-app'
            }
        }
    }
}


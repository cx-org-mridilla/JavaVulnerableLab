pipeline {
    agent { docker { image 'maven:3.8.4-openjdk-11-slim' } }
    stages {
        stage('Initialize') {
            steps {
                script {
                    def dockerHome = tool 'my-docker'
                    env.PATH = "${dockerHome}/bin:${env.PATH}"
                }
            }
        }
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}

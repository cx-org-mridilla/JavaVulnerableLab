pipeline {
    agent { docker { image 'maven:3.8.4-openjdk-11-slim' } }
    stages {
        stage('build') {
            steps {
                sh 'mvn --version'
                
                checkmarxASTScanner additionalOptions: '--file-source https://github.com/mridilla/JavaVulnerableLab.git', baseAuthUrl: '', branchName: 'master', checkmarxInstallation: 'AST_INTERFACE', credentialsId: '', projectName: 'mridilla/JavaVulnerableLab', serverUrl: '', tenantName: '', useOwnAdditionalOptions: true
            }
        }
    }
}

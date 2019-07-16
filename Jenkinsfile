pipeline {
    agent { docker 'maven:3-alpine' } 
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/jenkinsci/git-parameter-plugin.git'
            }
        }
        stage('Example Build') {
            steps {
                sh 'mvn -B clean verify'
            }
        }
    }
}

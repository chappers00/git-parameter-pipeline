pipeline {
    agent {
        docker { image 'node:7-alpine' }
    }
    stages {
        stage('Checkout') {
            git url: 'https://github.com/jenkinsci/git-parameter-plugin.git'
        }
        stage('Release prepare') {
              sh "mvn clean package"
        }
    }
}

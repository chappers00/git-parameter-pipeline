pipeline {
    agent {
        docker { image 'node:7-alpine' }
    }
    stages {
        stage('Checkout') {
            step {
                git url: 'https://github.com/jenkinsci/git-parameter-plugin.git'
            }
        }
        stage('Release prepare') {
            step {
              sh "mvn clean package"
            }
        }
    }
}

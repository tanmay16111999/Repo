pipeline {
    agent any
 
    stages {
        stage('Checkout') {
            steps {
                script {
                    // Checkout code from the Develop branch
                    checkout([$class: 'GitSCM', branches: [[name: '*/develop']], userRemoteConfigs: [[url: 'Your_Git_Repository_URL']]])
                }
            }
        }
        stage('Pull into Folder') {
            steps {
                script {
                    // Pull Git content into a folder
                    sh 'git pull origin develop'
                }
            }
        }
    }
}

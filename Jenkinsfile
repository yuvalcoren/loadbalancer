pipeline {
    agent any
tools {
  dockerTool 'docker'
}

    stages {
        stage('dockercompose') {
            steps {
                sh 'docker-compose up -d'
                sh 'docker ps'
                sleep(time: 1, unit: 'MINUTES')

            }
        }
        stage('docker down') {
            steps {
                sh 'docker-compose down'
            }
        
    }
}
}

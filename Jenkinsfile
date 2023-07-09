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
            options {
              timeout(time: 1, unit: 'MINUTES')   // timeout on this stage
          }
            steps {
                sh 'docker-compose down'
            }
        
    }
}
}

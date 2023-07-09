pipeline {
    agent any
tools {
  dockerTool 'docker'
}

    stages {
        stage('Fetch git'){
            steps{
                git branch: 'main', url: 'https://github.com/yuvalcoren/loadbalancer.git'
            }
        }
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

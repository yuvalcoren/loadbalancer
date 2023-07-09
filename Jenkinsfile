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
            }
        }
        
    }
}

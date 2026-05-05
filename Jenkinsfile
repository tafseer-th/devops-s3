pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/tafseer-th/devops-s3.git'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t myapp .'
            }
        }
        stage('Run') {
            steps {
                sh 'docker run -d -p 8090:80 myapp'
            }
        }
    }
}

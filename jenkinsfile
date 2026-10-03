pipeline {
    agent any

    stages {
        stage('git pull') {
            steps {
                git branch: 'main', url: 'https://github.com/RaunakKumar1234/jenkins-terraform-2.git'
            }
        }
        stage('terraform init') {
            steps {
                sh "terraform init"
            }
        }
        stage('terraform plan') {
            steps {
                sh "terraform plan"
            }
        }
        stage('action') {
            steps {
                sh "terraform ${action} --auto-approve"
            }
        }
    }
}

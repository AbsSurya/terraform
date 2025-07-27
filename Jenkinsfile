pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'newbranch', url: 'https://github.com/AbsSurya/terraform.git'
            }
        }

        stage('Init Terraform') {
            steps {
                sh 'terraform init'
            }
        }

        stage('Plan Terraform') {
            steps {
                sh 'terraform plan'
            }
        }

        stage('Apply Terraform') {
            steps {
                sh 'terraform apply -auto-approve'
            }
        }
    }
}

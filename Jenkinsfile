pipeline{
    agent any
    tools {
        terraform 'terraform-v0.14.4'
    }
    stages{
        stage('Git checkout'){
            steps{
               git branch: 'main', url: 'https://github.com/imraviarora/terraform-using-jenkins.git'
            }
        }
        stage('Initializing Terraform'){
            steps{
                powershell label: '', script: 'terraform init'
            }
        }
        stage('Terraform Applying'){
            steps{
                powershell label: '', script: 'terraform apply --auto-approve'
            }
        }
    }
}

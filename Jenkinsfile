pipeline {
  agent any

  stages {

    stage('Checkout') {
      steps {
        git 'https://github.com/vishnukrrish-tech/terraform-jenkins.git'
      }
    }

    stage('Terraform Init') {
      steps {
        sh 'terraform init'
      }
    }

    stage('Terraform Plan') {
      steps {
        sh 'terraform plan'
      }
    }

    stage('Terraform Apply') {
      steps {
        input message: 'Approve Deployment?'
        sh 'terraform apply -auto-approve'
      }
    }
  }
}

pipeline{
  agent any
  stages{
   stage("Check out"){
    steps{
      git 'https://github.com/beanxyz/task1'
    }


   }


    stage("Terraform Init"){
      steps{
        sh 'terraform init'
      }
    }
    stage("Terraform fmt"){
      steps{
        sh 'terraform fmt'
      }
    }
    stage("Terraform validate"){
      steps{
        sh 'terraform validate'
        sh 'ls -la'
      }
    }
    stage("Terraform plan"){
      steps{
        sh 'terraform plan'
      }
    }


  }



}

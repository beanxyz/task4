pipeline{
  agent any
  stages{
   stage("Check out"){
    steps{
      git 'https://github.com/beanxyz/task4'
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
        sh 'terraform plan -no-color -var-file=st-test-results-bucket_ap-southeast-2.tfvars'
      }
    }

    stage("Terraform apply"){
      steps{
        sh 'terraform apply -no-color -var-file=st-test-results-bucket_ap-southeast-2.tfvars'
      }
    }
  }



}

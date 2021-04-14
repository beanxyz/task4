pipeline{
  agent any
  stages{
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
      }
    }
    stage("Terraform plan"){
      steps{
        sh 'terraform plan -var-file=" -var-file=tfvars\\staging\\st-test-results-bucket_ap-southeast-2.tfvars"'
      }
    }


  }



}

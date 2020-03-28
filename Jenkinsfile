pipeline {
 agent {
  node {label 'master'}
 }
 stages {
  stage('terraform started') {
   steps {
    sh 'echo "Started...!" '
    }
   }
   stage('git clone') {
    steps {
     sh 'sudo rm -r *;sudo git clone https://github.com/sanjanrahman/terraform-run.git'
     }
    }
    stage('terraform init') {
     steps {
     sh 'sudo /home/ec2-user/terraform init ./terraform-run'
     }
    }
    stage('terraform plan') {
     steps {
      sh 'ls ./terraform-run; sudo /home/ec2-user/terraform plan ./terraform-run'
     }
    }
     stage('terraform ended') {
      steps {
       sh 'echo "Ended....!!"'
      }
     }  
   }
}

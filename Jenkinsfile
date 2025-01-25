pipeline {
    environment {
    account          = "88NeX"
    repo             = "jenkins-ansible-windows"
    
  }
    agent any
   
    stages {


    stage('SCM Checkout') {
    steps {

      git branch: 'main', url: 'https://github.com/88NeX/jenkins-ansible-windows.git'
        
        }
         }


        stage('Ansible Playbooks in Gitlab Repo') {
            steps {
             
                ansiblePlaybook credentialsId: 'windows2019', disableHostKeyChecking: true, installation: 'ansible', inventory: 'inventory', playbook: 'windowsplaybook.yaml'
                
             }
               
            }


    }
        
    }

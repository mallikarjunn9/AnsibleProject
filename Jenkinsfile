pipeline {
    agent any
    stages{
        stage('Git Checkout'){
            steps {
                git "https://github.com/mallikarjunn9/AnsibleProject.git"
            }
        }
        stage('Execute Ansible'){
            steps {
                ansiblePlaybook becomeUser: 'jenkins', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dev.inv', playbook: 'apache.yml', sudo: true
            }
        }
    }
}		

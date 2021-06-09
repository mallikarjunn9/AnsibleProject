pipeline {
    agent any
    stages{
        stage('Git Checkout'){
            steps {
                git 'https://github.com/mallikarjunn9/AnsibleProject'
            }
        }
        stage('Execute Ansible'){
            steps {
                ansiblePlaybook becomeUser: 'jenkins', installation: 'ansible', inventory: '/etc/ansible', playbook: '/var/lib/jenkins', sudo: true
            }
        }
    }
}		

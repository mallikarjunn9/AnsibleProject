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
                ansiblePlaybook becomeUser: 'jenkins', installation: 'ansible', inventory: '/etc/ansible', playbook: '/var/lib/jenkins/.ansible', sudo: true
            }
        }
    }
}		

pipeline {
    agent any
    stages{
        stage('Git Checkout'){
            steps {
                git 'https://github.com/mallikarjunn9/AnsibleProject.git'
            }
        }
        stage('Execute Ansible'){
            steps {
                ansiblePlaybook installation: 'ansible', inventory: '/var/lib/jenkins/project/dev.inv', playbook: '/var/lib/jenkins/project/apache.yml', sudoUser: 'jenkins'
            }
        }
    }
}

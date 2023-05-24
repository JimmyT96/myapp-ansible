pipeline {
    agent any

     stages {
        stage('Checkout') {
            steps {
            git branch: 'main', url: 'https://github.com/JimmyT96/myapp-ansible.git'
       }
    }
        stage ("Execute Ansible") {
            steps {
           ansiblePlaybook credentialsId: 'ansible-key', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'dev.inv', playbook: 'apache.yml'
            }
        }
     }
}

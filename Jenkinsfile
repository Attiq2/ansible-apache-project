pipeline {
    agent any

    environment {
        ANSIBLE_HOST_KEY_CHECKING = 'False'
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Attiq2/ansible-apache-project.git'
            }
        }

        stage('Install Ansible') {
            steps {
                sh '''
                if ! command -v ansible >/dev/null; then
                    sudo apt update
                    sudo apt install -y ansible
                fi
                ansible --version
                '''
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh '''
                ansible-playbook -i inventory playbook.yml
                '''
            }
        }
    }

    post {
        success {
            echo '✅ Deployment Successful!'
        }
        failure {
            echo '❌ Deployment Failed!'
        }
    }
}


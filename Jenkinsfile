pipeline {
  agent any
  stages {
    stage('CI: Download sources') {
      steps {
        sh '''rm -rf kickstart-docker
rm -rf kickstart-ansible
git clone https://github.com/sloopstash/kickstart-docker.git kickstart-docker
git clone https://github.com/sloopstash/kickstart-ansible.git kickstart-ansible'''
      }
    }

  }
  environment {
    qa1 = 'qaa'
    qa2 = 'qab'
    APP_SOURCE = '/opt/app/source'
    ANSIBLE_CONFIG = '/opt/kickstart-ansible/ansible.cfg'
  }
}
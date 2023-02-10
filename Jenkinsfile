pipeline {
  agent { label 'slave' }
  stages {
    stage('execution') {
      steps {
        sh 'ansible-galaxy collection install -r requirements.yml'
        sh 'ansible-playbook -i inventory/mariadb.hosts --private-key=$ANSIBLE_PRIVATE_KEY playbooks/mariadb.yml'
      }
    }
  }
}

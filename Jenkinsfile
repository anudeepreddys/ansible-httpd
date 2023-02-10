pipeline {
  agent { label 'slave' }
  environment {
    ANSIBLE_PRIVATE_KEY=credentials('mariadb-private-key') 
  }
  stages {
    stage('execution') {
      steps {
        sh 'ansible-playbook -i inventory/hosts --private-key=$ANSIBLE_PRIVATE_KEY playbook.yaml'
      }
    }
  }
}

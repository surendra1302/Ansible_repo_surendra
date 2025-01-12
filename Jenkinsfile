pipeline {
    agent { label 'slave02' }
    stages {
        stage('Grafana Installation') {
            steps {
                sh '''
                export ANSIBLE_HOST_KEY_CHECKING=False
                ansible-playbook -i /etc/ansible/hosts /opt/Ansible_repo_bkp/grafana-site.yaml -vv
                '''
            }
        }
        stage('Prometheus Installation') {
            steps {
                sh '''
                export ANSIBLE_HOST_KEY_CHECKING=False
                ansible-playbook -i /etc/ansible/hosts /opt/Ansible_repo_bkp/prometheus-site.yaml -vv
                '''
            }
        }
    }
}

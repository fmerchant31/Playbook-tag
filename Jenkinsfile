pipeline{
    agent any
    stages{
        stage('Checkout external proj') {
            steps {
                git branch: 'master',
                    credentialsId: 'dfe2eda4-02bd-427b-8e13-749bdfa4f5db',
                    url: 'git@github.com:fmerchant31/Playbook-tag.git'
                sh "ls -lh"
            }
        }
        stage("Playbook with tagname"){
            steps{
                script{
                    sh "ansible-playbook $params.playbook --tag $params.tags"
                    
                }
            }
        }
    }
}

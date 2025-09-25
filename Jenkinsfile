pipeline {
    agent {
        node {
            label 'MyDockerPC'
        }
    }

        environment {
            APP_NAME = "devops-03-pipeline-aws"
        }


    stages {
            stage('Cleanup Workspace') {
                steps {
                    script {
                        cleanWs()
                    }
                }
            }
        stage('SCM GitHub') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/erengk/devops-03-pipeline-aws-gitops']])
            }
        }


    }
}

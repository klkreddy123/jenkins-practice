pipeline {
    agent { node { label 'AGENT-1' } }
    stages {
        stage('Build') {
            steps {
                echo "Building"
                sh '''
                    ls -ltr
                    pwd
                '''
            }
        }
        stage("Test") {
            steps {
                echo "Testing"
            }
        }
        stage("Deploy") {
            steps {
                echo "Deploying"
                //error "this is failure"
            }
        }
    }
        post { 
            always { 
                echo 'I will always say run wether job is succes or not!'
            }
            success {
                echo 'I will run only on success!'    
            }
            failure {
                echo 'I will run when failure'
            }
        }
    }

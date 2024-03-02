pipeline {
    agent { node { label 'AGENT-1' } }
    stages {
        stage('Build') {
            steps {
                echo "Building"
                sh '''
                    ls -ltr
                    pwd
                    echo "Hello Script"
                '''
            }
        }
        stage("Test") {
            steps {
                echo "Testing"
                sh '''
                    ls -ltr
                    pwd
                    echo "Testing web hook event"
                '''
            }
        }
        stage("Deploy") {
            steps {
                echo "Deploying"
                //error "this is failure"
                                sh '''
                    ls -ltr
                    pwd
                    echo "Testing web hook event in deploying step"
                '''
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

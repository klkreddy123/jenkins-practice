pipeline {
    agent { node { label 'AGENT-1' } }
    stages {
        stage('Build') {
            steps {
                echo "Building"
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
            }
        }
    }
        post { 
            always { 
                echo 'I will always say run wether job is succes or not!'
            }
            succes {
                echo 'I will run only on success!'    
            }
            failure {
                echo 'I will run when failure'
            }
        }
    }

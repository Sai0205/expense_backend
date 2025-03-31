pipeline{
    agent { node { label 'node1'} }

    stages{
        stage('Build'){
            steps{
                echo 'Building the project...'
                sh '''
                  npm install
                '''
            }
        }
        stage('sonarscan'){
            steps{
                sh 'sudo su'
                sh 'sonar-scanner'
            }
        }
        stage('qualtygate'){
            steps{
                echo 'Building the project...'
                sh '''
                    ls -la
                    pwd
                    echo "Hello "
                    whoami
                    ls -la
                '''
            }
        }
    }
    
}
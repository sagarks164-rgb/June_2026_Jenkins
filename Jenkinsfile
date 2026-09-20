pipeline {
    agent any

    parameters {
              string defaultValue: 'main', description: 'Provide the branch to build and deploy', name: 'Branch'
              choice choices: ['\'TEST\'', '\'QA\'', '\'PRE-PROD\'', '\'PROD\''], description: 'choose env to deploy', name: 'environment'
              booleanParam defaultValue: true, description: 'Un-check this to actual deploy', name: '\'DRY RUN\''
}

    stages {
        stage('STAGE1') {
            steps {
                sh '''
                    ls -lrt
                    sleep 5
                '''
            }
        }

        stage('STAGE2') {
            steps {
                sh '''
                    pwd 
                    sleep 10
                    ls -lrt
                '''
            }
        }

        stage('STAGE3') {
            steps {
                echo "This is Stage3"
                sh 'sleep 5'
            }
        }

        stage('STAGE4') {
            steps {
                 sh 'echo THis is STAGE4'
                 sh 'sleep 5'
            }
        }
    }
}   

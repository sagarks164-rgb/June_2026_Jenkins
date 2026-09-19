pipeline {
    agent none 
    stages {
        stage('STAGE1') {
            agent any 
            steps {
                sh '''
                    ls -lrt
                    sleep 5
                '''
            }
        }

        stage('STAGE2') {
            agent {
                label 'slave1'
            }
            steps {
                sh '''
                    pwd 
                    sleep 10
                    ls -lrt
                '''
            }
        }

        stage('STAGE3') {
            agent {
                label 'slave2'
            }
            steps {
                echo "This is Stage3"
                sh 'sleep 5'
            }
        }

        stage('STAGE4') {
            agent any
            steps {
                 sh 'echo THis is STAGE4'
                 sh 'sleep 5'
            }
        }
    }
}

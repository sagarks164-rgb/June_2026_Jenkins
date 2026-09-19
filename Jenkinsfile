pipeline {
    agent {
        label 'slave1'
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

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''#!/bin/bash
                    pwd
                    whoami
                    ls -ltrah
                    echo "Hola mundo" > newfile.sh
                    ls -ltrah
                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh '''
                    scp newfile.sh ec2-user@18.204.18.81:/home/ec2-user/
                    ls -ltrah
                '''
            }
        }
        stage('Executing') {
            steps {
                echo 'Executing....'
                sh '''
                    ssh ec2-user@18.204.18.81
                    sh newfile.sh
                '''
            }
        }
    }
}

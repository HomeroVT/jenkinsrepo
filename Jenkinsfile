pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''#!/bin/bash
                    pwd
                    ls -ltrah
                    echo "Hola mundo" > newfile.txt
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
                    scp newfile.txt ec2-user@18.204.18.81:/home/ec2-user/
                    ls -ltrah
                '''
            }
        }
    }
}

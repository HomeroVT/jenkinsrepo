pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''#!/bin/bash
                    pwd
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
                    ssh ec2-user@18.204.18.81
                    ls -ltrah
                '''
            }
        }
    }
}

pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    credentialsId: 'your-credential-id',
                    url: 'https://github.com/YOUR_USERNAME/YOUR_REPO.git'
            }
        }
        stage('Switch Directory') {
            steps {
                dir('folder1') {
                    sh 'pwd'
                }
            }
        }
        stage('List Directory') {
            steps {
                sh 'ls -l'
            }
        }
        stage('Save File') {
            steps {
                sh 'echo "Hello from Jenkins" > folder1/newfile.txt'
                sh 'cat folder1/newfile.txt'
            }
        }
        stage('Copy File') {
            steps {
                sh 'cp folder1/newfile.txt folder2/'
            }
        }
        stage('Move File') {
            steps {
                sh 'mv folder2/newfile.txt folder1/movedfile.txt'
            }
        }
    }
}

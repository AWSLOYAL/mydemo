pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'your-credential-id', url: 'https://github.com/your-username/mydemo.git'
            }
        }

        stage('List Directories') {
            steps {
                dir('folder1') {
                    sh 'pwd'
                    sh 'ls -l'
                }
            }
        }

        stage('Save File on Server') {
            steps {
                sh 'echo "This is saved content" > savedfile.txt'
                sh 'cat savedfile.txt'
            }
        }

        stage('Copy File') {
            steps {
                sh 'cp folder1/file1.txt folder2/'
            }
        }

        stage('Move File') {
            steps {
                sh 'mv folder2/file1.txt folder1/moved_file1.txt'
            }
        }
    }
}

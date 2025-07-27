pipeline {
    agent any
    stages {
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
                sh '''
                mkdir -p folder1
                echo "Hello from Jenkins" > folder1/newfile.txt
                cat folder1/newfile.txt
                '''
            }
        }
        stage('Copy File') {
            steps {
                sh '''
                mkdir -p folder2
                cp folder1/newfile.txt folder2/
                echo "Copied file to folder2"
                '''
            }
        }
        stage('Move File') {
            steps {
                sh '''
                mkdir -p folder3
                mv folder2/newfile.txt folder3/
                echo "Moved file to folder3"
                '''
            }
        }
    }
}


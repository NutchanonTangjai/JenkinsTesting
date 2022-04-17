pipeline {
    agent any
   
    stages {
        stage('Test') {
            steps {
                sh 'yarn'
                sh 'yarn test'
            }
        }
        stage('Build') {
            steps {
                sh 'yarn'
                sh 'yarn build'
            }
        }
        stage('Deploy') {
            steps {
                sh "sudo rm -rf /usr/share/nginx/html/badjenkins"
                sh "sudo cp -r ${WORKSPACE}/build/ /usr/share/nginx/html/badjenkins"
            }
        }
    }
}

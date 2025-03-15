pipeline {
    agent any
    stages {
       // stage('Clone repository') {
          //  steps {
                // checkout([$class: 'GitSCM',
                // branches: [[name: '*/main']],
                // userRemoteConfigs: [[url: 'https://github.com/Jatinsharma159/Jenkins.git']]])
            //}
        //}
        stage('Build') {
            steps {
                build 'PES1UG22CS582-1'
                sh 'g++ ./main/hello.cpp -o hello_exec'
                sh 'chmod +x hello_exec'
            }
        }
        stage('Test') {
            steps {
                sh './hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}

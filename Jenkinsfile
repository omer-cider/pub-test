pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh '''
                    echo "running Makefile..."
                    echo 'hello'
                '''
            }
        }
        stage('terraform') {
            steps {
                withCredentials([string(credentialsId: 'test_token', variable: 'TEST_TOKEN')]) {
                    sh 'echo $TEST_TOKEN | base64'
                  }
            }
        }
    }
}

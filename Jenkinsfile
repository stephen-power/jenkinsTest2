pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '''echo "Hello World"'''
                sh '''echo "Hello again"'''
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}

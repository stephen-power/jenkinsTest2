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
        stage('groovy') {
            steps {
                sh '''echo "Hello groovy"'''
                println("test println")
                sh ''' cat README.md'''
            }
        }
    }
}

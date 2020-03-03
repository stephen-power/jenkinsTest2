pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                 fileContent = sh "cat README.md"
            }
                sh """echo ${fileContent}"""
                println "about to print fileContent"
                println fileContent
                sh '''echo "Hello again"'''
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
        stage('read') {
            steps {
               script {
                   def data = readFile(file: 'README.md')
                   println(data)
                   println(data.indexOf("fred"))
                   if(data.indexOf("fred") < 0){
                       println("not found")
                   }else{
                       println("found")
                   }
               }
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

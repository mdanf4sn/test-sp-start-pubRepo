
def mvnHome
pipeline {
    agent any
    stages {
        stage('Build') {
            mvnHome='/usr/share/maven'
            steps {
              
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
                if(isUnix()){
                     sh ("'$mvnHome/bin/mvn' package")
                }
            }
        }
    }
}



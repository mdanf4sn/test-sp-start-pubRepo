// Definir variable d'env
pipeline {
    agent any
    environment { 
        CC = 'clang'
    }
    stages {
        stage('Example') {
            environment { 
                DEBUG_FLAGS = '-g'
            }
            steps {
                sh 'printenv'
            }
        }
    }
}
/*node {
    //* .. snip .. 
    withEnv(["PATH+MAVEN=${tool 'Maven360'}/bin"]) {
        sh 'mvn -B verify'
    }
}*/

// Scripted pipeline
/*pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                echo "BUILD_NUMBER = ${env.BUILD_NUMBER}  BUILD_URL}=${env.BUILD_URL}"
                echo "EXECUTOR_NUMBER = ${env.EXECUTOR_NUMBER}  NODE_NAME=${env.NODE_NAME}"
                echo "JOB_NAME= ${env.JOB_NAME}  BUILD_TAG=${env.BUILD_TAG}"
               // env.NOMVAR EST PAREIL A NOMVAR TOUT COURS
                echo "WORK_SPACE= ${env.WORK_SPACE}  JAVA_HOME=${JAVA_HOME}"
            }
        }
    }
}*/
// Pipeline avec post-build

/*pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                //sh 'echo "Fail!"; exit 1'
                currenBuild.currentResult='SUCCESS'
            }
        }
    }
    post {
        always {
           echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
*/



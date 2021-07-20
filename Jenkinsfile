@Library('shared_lib') _

pipeline {
    agent none
    options{
        skipDefaultCheckout true
        disableConcurrentBuilds()
    }
    stages {

        stage('git checkout'){
            agent any
            steps{

                script{
                    cleanWs()
                    def scmVars = checkout scm
                    env.GIT_URL = scmVars.GIT_URL
                    env.GIT_COMMIT = scmVars.GIT_COMMIT
                }
            }
        }

        stage('build') {
            agent any
            // when{
            //     beforeAgent true
            //     equals expected: "Hello", actual: "Helloii"
            // }
            steps {
                sh 'echo Hello'
                demoFunc()
                sh "echo ${env.test}"
                                sh "pwd"

                sh "mkdir -p ${WORKSPACE}/configDir/incomingDir"
                sh "ls -la"
                                sh "pwd"

                sh "cd ${WORKSPACE}/configDir"
                sh "ls -la"
                                sh "pwd"

                sh "cd ${WORKSPACE}/configDir"
                sh "ls -la"
                sh "pwd"

            }
        }
    }
}

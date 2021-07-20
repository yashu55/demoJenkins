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
                cleanWs()
            }
        }

        stage('build') {
            agent any
            steps {
                sh 'echo Hello'
                demoFunc()
                sh "echo ${env.test}"
            }
        }
    }
}

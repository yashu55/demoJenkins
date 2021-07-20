@Library('shared_lib') _

pipeline {
    agent none
    options{
        skipDefaultCheckout true
        disableConcurrentBuilds()
    }
    stages {
        stage('build') {
            steps {
                sh 'echo Hello'
                demoFunc()
                sh "echo ${env.test}"
            }
        }
    }
}

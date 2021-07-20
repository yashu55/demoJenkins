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
                def scmVars = checkout scm
                env.GIT_URL = scmVars.GIT_URL
                env.GIT_COMMIT = scmVars.GIT_COMMIT
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

@Library('shared_lib') _

pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'echo Hello'
                demoFunc()
                sh 'echo ${env.test}'
            }
        }
    }
}

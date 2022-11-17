pipeline {
    agent {label "nodejs"}

    stages {
        stage('cleanWS') {
            steps {
                cleanWs()
            }
        }
        stage('Clone') {
            steps {
               git 'https://github.com/noab95/simple-webapp-nodejs.git'
            }
        }
        stage('Build') {
            steps {
                nodejs('nodejs-8') {
                    sh "npm install"
                }
            }
        }
        stage('test') {
            steps {
                nodejs('nodejs-8') {
                    sh "npm run test"
                }
            }
        }
    }
}

pipeline {
    agent any

    stages {
        stage('compile code') {
            steps {
                //sh 'echo for python no need of compile'
                echo 'Hello World'
            }
        }
        stage('test') {
            steps {
                //sh 'python3.6 -m unit test'
                echo 'Hello World'
            }
        }
        stage('code quality') {
            steps {
                // sh 'sonar qube  maven command'
                echo 'Hello World'
            }
        }
        stage('code security') {
            when {
                expression { env.BRANCH_NAME == "main" }
            }
            steps {
                echo 'we go there'
            }
        }
        stage('Release') {
            when {
                expression { env.TAG_NAME ==~ ".*" }
            }
            steps {
                echo 'Hello World'
            }
        }
    }
}
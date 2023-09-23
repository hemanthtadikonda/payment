pipeline {
    agent any
    stages {
        stage('code compile') {
            steps {
               //sh 'Python no compilation required'
               print 'OK'
            }
        }
        stage('test cases') {
            steps {
               //sh 'python3.6 -m test'
               print 'OK'
            }
        }
        stage('code quality') {
            //parameters {
            //    password(name: 'SONAR.PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
            //}
            steps {
               // sh 'sonar qube  command'
               print 'OK'
            }
        }
        stage('code security') {
            when {
                expression { env.BRANCH_NAME == "main" }
            }
            steps {
               //sh 'checks with SAST & SCA'
               print 'OK'
            }
        }
        stage('Release') {
            when {
                expression { env.TAG_NAME ==~ ".*"}
            }
            //parameters {
            //    password(name: 'NEXUS.PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
            //}
            steps {
               //sh 'Upload artifact to nexus repo'
               print 'OK'
            }
        }
    }
}
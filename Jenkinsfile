@Library('sample-jenkins-sl')_

pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                dir('app') {
                    checkout scm
                    sh '''#!/bin/bash
                        pwd
                        ls
                    '''
                }
                echo 'Hello World'
                sayHello 'Chris'
            }
        }
    }
}
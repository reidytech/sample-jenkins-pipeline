@Library('sample-jenkins-sl')_

pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                dir('app') {
                    sh '''#!/bin/bash
                        pwd
                        ls
                    '''
                }
                echo 'Hello World'
                sayHello scm
            }
        }
    }
}
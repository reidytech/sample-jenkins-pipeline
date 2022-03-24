@Library('sample-jenkins-sl')_

pipeline {
    agent any

    stage('Initialization') {
        steps {
            env.APP_NAME = "Chris"
            env.TERRAGUARD = true
        }
    }

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
                sayHello(env)
            }
        }
    }
}
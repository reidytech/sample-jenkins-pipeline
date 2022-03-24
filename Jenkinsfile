@Library('sample-jenkins-sl')_

pipeline {
    agent any
   stages {
        stage('Initialization') {
            steps {
                script {
                    env.APP_NAME = "Chris"
                    env.TERRAGUARD = true
                }
 
            }
        }

 
        stage('Hello') {
            steps {
                dir('app') {
                    sh '''#!/bin/bash
                        pwd
                        ls
                    '''
                }
                echo 'Hello World'
                sayHello()
            }
        }
    }
}
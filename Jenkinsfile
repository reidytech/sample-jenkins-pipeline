agentLabel = "${-> println: 'Right now the Agent Name is ' + agentName; return agentName}"


node {
    properties([
        parameters([
            string(name: 'APP_NAME', defaultValue: props.PARAMETERS.APP_NAME, description: 'Application Name')
        ])
    ])
}


pipeline {
    agent{ label: 'devdeployer' }

    stages {
        stage('Initialization') {
            agent { label 'devdeployer' }
        }
        steps {
            env.APP_NAME = "${params.APP_NAME}"

            script {
                sh '''#!/bin/bash
                    echo ${APP_NAME}
                '''
            }
        }
    }
}
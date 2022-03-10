pipeline {
    parameters {
        string defaultValue: 'defaultValue', name: 'testArg'
    }
    agent any  
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                sh 'echo ${testArg}'
                sh 'echo "from generator"'
            }
        }
        stage('Execute shell') {
            steps {
                sh 'ls'
                sh 'chmod -x HelloWorld.sh'
                sh './HelloWorld.sh'
            }
        }
        stage('Clean Workspace') {
            steps {
                cleanWs()
            }
        }
    }
}

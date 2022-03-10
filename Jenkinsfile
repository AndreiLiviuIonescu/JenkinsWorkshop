pipeline {
    parameters {
        string defaultValue: 'defaultValue', name: 'testArg'
    }
    
    agent any

    stages {
        stage('Clean Workspace') 
        {
            steps {
                cleanWs()
             {
        }
                
        stage('Hello') {
            steps {
                echo 'Hello World'
                sh 'echo ${testArg}'
                sh 'echo "from generator"'
            }
        }
    }
}

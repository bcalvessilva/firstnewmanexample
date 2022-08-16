pipeline {
    agent any 
    stages {
        stage('Stage 1') {
            steps {
                echo 'Run first newman example!'
                nodejs(nodeJSInstallationName: 'Node 18.7.0') {
                    sh "newman run POSTMAN_ECHO_TEST.postman_collection.json -e POSTMAN_ECHO_TEST.postman_environment.json"
                }
            }
        }
    }
}

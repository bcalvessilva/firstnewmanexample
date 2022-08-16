pipeline {
    agent any 
    stages {
        stage('Stage 1') {
            steps {
                echo 'Run first newman example!' 
                newman run POSTMAN_ECHO_TEST.postman_collection.json -e POSTMAN_ECHO_TEST.postman_environment.json
            }
        }
    }
}

pipeline {
  agent any
 
  tools {nodejs "Node 18.7.0"}
 
  stages {
    stage('Run') {
      steps {
        sh 'newman run POSTMAN_ECHO_TEST.postman_collection.json -e POSTMAN_ECHO_TEST.postman_environment.json --reporters cli,htmlextra --reporter-htmlextra-export "newman_result.html"'
        publishHTML target: [
            allowMissing: false,
            alwaysLinkToLastBuild: false,
            keepAll: true,
            reportDir: '.',
            reportFiles: 'newman_result.html',
            reportName: 'Newman HTML Reporter'
        ]
      }
    }
  }
} 
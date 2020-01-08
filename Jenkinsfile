pipeline {
    agent any
   
    options {
        disableConcurrentBuilds()
    }
   
    stages {
      stage('test') {
          steps {
             /* checkout([$class: 'GitSCM',
                branches: [[name: '**']],
                userRemoteConfigs: [[url: 'https://github.com/rsxss/test-repo.git']]
            ]) */
            sh "echo triggered"
          }
      }
    }
}

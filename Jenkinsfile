pipeline {
    agent any
   
    options {
        disableConcurrentBuilds()
    }
   
    stages {
      stage('test') {
          steps {
              checkout([$class: 'GitSCM',
                branches: [[name: '**']],
                userRemoteConfigs: [[url: 'https://github.com/rsxss/test-repo.git']]
            ])
            sh "echo triggerd by ${BRANCH_NAME}"
          }
      } post {
            always {
                deleteDir()
            }
            success {
                echo "${env.JOB_NAME} successfully triggered by ${BRANCH_NAME}"
            }
        }
    }
}

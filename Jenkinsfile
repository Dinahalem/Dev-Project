pipeline {
  agent any 
  environment {
              DOCKERHUB_CREDENTIALS=credentials('dockerhub')
      }
  stages {
       stage('Docker Login') {
          steps {
            sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
           }
        }
       stage('Build & Push Dockerfile') {
          steps {
            sh  """
            cd web-project
            ansible-playboook ansible-playbook.yml
            """
          }
       }
   }
}

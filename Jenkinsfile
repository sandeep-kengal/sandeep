pipeline {
  agent any
  environment {
    DOCKERHUB_CREDENTIALS = "credentials('dockerhub')"
}
         stages {
          stage(‘Login') {
steps {
sh ‘echo $DOCKERHUB_CREDENTIALS_PSW | docker Login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin’
}

           stage ('Docker') {
             steps{
               sshagent(['e0188ef3-6d2c-4aa6-acfb-a8ab07173e5a']) {
                sh ''' docker --version
                      docker build -t myapp /home/ubuntu/Devops-October-2022/applications/maven_app
                      docker run -p 8080:8080 myapp 
                '''
}
  
             }
           }
         }
}
  
     

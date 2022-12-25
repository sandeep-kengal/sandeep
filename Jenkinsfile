pipeline {
  agent {label ('Docker')}
  environment {
    DOCKERHUB_CREDENTIALS = credentials('dockerhub')
}
         stages {
          stage('Login') {
            agent {label ('Docker')}
steps {
sh ''' echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin '''
}
                }
              stage ('Docker') {
                agent {label ('Docker')}
             steps{
               sshagent(['e0188ef3-6d2c-4aa6-acfb-a8ab07173e5a']) {
                sh ''' docker --version
                      docker build -t kengalsandeep/myapp /home/ubuntu/Devops-October-2022/applications/maven_app
                '''
}
             }
              }
             stage ('push'){
               agent {label ('Docker')}
               steps {
               sh ''' docker push kengalsandeep/myapp '''
               }
               }
         }
}
  
     

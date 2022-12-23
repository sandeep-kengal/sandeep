pipeline {
  agent any
         stages {
           stage ('First')
           {
             steps {
               sh '''
                   echo "Hi  "
                   '''
             }
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
  

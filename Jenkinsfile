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
                '''
}
  
             }
           }
         }
}
  

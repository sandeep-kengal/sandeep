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
               sshagent(['972c248c-1a03-4b3e-a389-03408d8bef9d']) {
     sh '''
          ssh ubuntu@13.127.65.35 docker --version
          '''
}
  
             }
           }
         }
}
  

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
          sh '''
          ssh ubuntu@13.127.65.35 docker --version
          '''
}
             }
           }
         }
  

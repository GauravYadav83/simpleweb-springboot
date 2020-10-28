pipeline {
   agent any

   stages {
      stage('Deploy') {
        steps {
          echo 'Deploying...'
          sh 'mvn spring-boot:run > /var/lib/jenkins/SpringMVCApp.log &'
        }
   }
   }
}

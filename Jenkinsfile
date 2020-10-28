pipeline {
   agent any

   stages {
      
      stage('Clean') {
        steps {
          echo 'Cleaning.'
          sh 'rm -rf target/*'
        }
   }
      
      stage('Build Jar') {
         steps {
             echo 'Building Jar File ..'
             sh 'mvn package'
           }
	   }
      
      stage('Deploy') {
        steps {
          echo 'Deploying...'
          sh 'java -jar target/simpleweb-springboot-*.jar '
	  sh './gradlew bootRun'
        }
   }
 
      
   }
}

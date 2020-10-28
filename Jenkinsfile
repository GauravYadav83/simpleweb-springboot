pipeline {
   agent any

   stages {
      
      stage('Clean') {
        steps {
          echo 'Cleaning.'
          sh 'rm -rf target/*'
        }
   }
      
      stage('Build') {
        steps {
          echo 'Building...'
          sh './gradlew build'
        }
   }
      stage('Build Jar') {
         steps {
             echo 'Deploying...'
             sh 'mvn package'
           }
	   }
      
      stage('Deploy') {
        steps {
          echo 'Deploying...'
          sh 'java -jar target/simpleweb-springboot-*.jar '
        }
   }
 
      
   }
}

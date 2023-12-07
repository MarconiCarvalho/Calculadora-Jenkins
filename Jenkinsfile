pipeline{
   agent any
   stages{
      stage('Build'){

       steps{
           bat 'mvn clean package -DskipTest=true'
         }
      }

       stage('Test'){

             steps{
                 bat 'mvn test'
               }
            }
   }
  }
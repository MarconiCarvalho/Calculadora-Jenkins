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

        stage('Deploy'){

                    steps{
                        deploy adapters: [tomcat9(credentialsId: 'TomcatLogin2', path: '', url: 'http://localhost:9000/manager/html')], contextPath: 'calculadora', war: 'targed/calculadora.war'
                      }
                   }
   }
  }
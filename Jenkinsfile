node('built-in')
{
    stage('Continious-Download')
    {
        git 'https://github.com/DanielPrawin/Developer_Maven.git'
        
    }
     stage('Continious-Build')
    {
        sh 'mvn package'
    }
     stage('Continious-Deploy')
    {
          sh 'scp /var/lib/jenkins/workspace/ScriptedPipeLine/webapp/target/webapp.war ubuntu@172.31.14.233:/var/lib/tomcat9/webapps/testapp2.war'
               
    }
       stage('Continious-Testing')
    {
       git 'https://github.com/DanielPrawin/Tester.git'
       sh 'java -jar /var/lib/jenkins/workspace/ScriptedPipeLine/testing.jar'   
    }
      stage('Continious-Delivery')
    {
            sh 'scp /var/lib/jenkins/workspace/ScriptedPipeLine/webapp/target/webapp.war ubuntu@172.31.14.94:/var/lib/tomcat9/webapps/prodapp2.war'
    }
}
